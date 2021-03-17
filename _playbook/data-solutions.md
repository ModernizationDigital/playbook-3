---
layout: page
title: 'The Microwizard'
---
The Microwizard base system runs inside of a VirtualBox VM. We provision the VM using Vagrant and then use a combination of shell scripts, Ansible playbooks, and custom code to smooth over the experience. Developers must be running a modern Linux distribution or Mac OS X (we’ve tested on Fedora 22 and OS 10.10 Yosemite) and should have the following software installed before trying to use Datawire Microwizard:


| Software    | Version    | Instructions |
| ----------- | ---------- | ------------ |
| Ansible     | &gt;=1.9.4 | `sudo pip install ansible` or see the official [install](http://docs.ansible.com/ansible/intro_installation.html) instructions |
| Vagrant     | &gt;=1.7.4 | [Install instructions](https://docs.vagrantup.com/v2/installation/index.html) |
| Virtual Box | &gt;= 5.0  |[Install instructions](https://www.virtualbox.org/wiki/Downloads) |

### To get started, do the following:

    <script src="https://d3js.org/d3.v5.min.js"></script>
    <script>
      const margin = {left: 0, right: 0, top: 0, bottom: 0},
          duration = 1000,
          categories = "abcdefg".split(""),
          colors = {};

      categories.forEach((d, i) => {
        colors[d] = d3.schemeSet2[i];
      });

      const svg = d3.select("body").append("svg");
      const g = svg.append("g");

      const pack = d3.pack()
          .padding(d => d.height * 5);

      let root = d3.hierarchy(makeData())
          .sum(d => d.value)
          .sort((a, b) => a.value - b.value);

      draw();
      d3.interval(_ => {
        root = d3.hierarchy(makeData())
          .sum(d => d.value)
          .sort((a, b) => a.value - b.value);

        draw();
      }, duration * 2);
      onresize = _ => draw(true);

      function draw(resizing){
        const diameter = Math.min(innerWidth, innerHeight),
            width = diameter - margin.left - margin.right,
            height = diameter - margin.top - margin.bottom;

        svg
            .attr("width", width + margin.left + margin.right)
            .attr("height", height + margin.top + margin.bottom);

        g
            .attr("transform", `translate(${margin.left}, ${margin.top})`);

        pack
            .size([width, height]);

        const node = pack(root),
            leaves = node.leaves(),
            ancestors = node.ancestors();

        const ancestorCircles = g.selectAll(".ancestor-circle")
            .data(ancestors[0].children, d => d.data.name);

        if (resizing){
          ancestorCircles
              .attr("cx", d => d.x)
              .attr("cy", d => d.y)
              .attr("r", d => d.r);
        }
        else {
          ancestorCircles
            .transition().duration(duration)
              .attr("cx", d => d.x)
              .attr("cy", d => d.y)
              .attr("r", d => d.r);          
        }

        ancestorCircles.enter().append("circle")
            .style("fill", d => colors[d.data.name])
            .style("stroke", d => colors[d.data.name])
            .attr("class", "ancestor-circle")
            .attr("cx", d => d.x)
            .attr("cy", d => d.y)
            .attr("r", 1e-6)
          .transition().duration(duration / 2)
            .attr("r", d => d.r);

        const leafCircles = g.selectAll(".leaf-circle")
            .data(leaves, d => d.data.name);

        if (resizing){
          leafCircles.exit()
              .attr("r", 1e-6)
              .remove();

          leafCircles
              .attr("cx", d => d.x)
              .attr("cy", d => d.y)
              .attr("r", d => d.r);
        }
        else {
          leafCircles.exit()
            .transition().duration(duration / 2)
              .attr("r", 1e-6)
              .remove();

          leafCircles
            .transition().duration(duration)
              .attr("cx", d => d.x)
              .attr("cy", d => d.y)
              .attr("r", d => d.r);
        }

        leafCircles.enter().append("circle")
            .style("fill", d => colors[d.parent.data.name])
            .style("stroke", d => colors[d.parent.data.name])
            .attr("class", "leaf-circle")
            .attr("cx", d => d.x)
            .attr("cy", d => d.y)
            .attr("r", 1e-6)
          .transition().duration(duration)
            .attr("r", d => d.r);
      }

      // Generate random hierarchical data
      function makeData(){
        return {
          name: "root",
          children: categories.map(name => {
            return {
              name,
              children: d3.range(randBetween(5, 10)).map((d, i) => {
                return {
                  name: `${name}${i}`,
                  value: randBetween(10, 100)
                }
              })
            }
          })
        };
      }

      function randBetween(min, max){
        return Math.floor(Math.random() * (max - min + 1) + min);
      }
    </script>