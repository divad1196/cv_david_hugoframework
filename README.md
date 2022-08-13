# My Website
* Using [H.U.G.O](https://gohugo.io/) framework
* Theme: [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/)
  This was added using subtree to fix the version and allow easy changes
  ```bash
  git subtree add --squash -P themes/PaperMod https://github.com/adityatelange/hugo-PaperMod.git master
  ```



## Custom configuration

* `overview: true` on a page: display it on the home page

* Support for [mermaid](https://mermaid-js.github.io/mermaid/#/) diagram ([official hugo tutorial](https://gohugo.io/content-management/diagrams/))

* Support for charts using `Chart.js` .
  Usage

  ```bash
  {{< chart id="basicChart" data=charts.example >}}
  ```

  Nb: The data will be taken from the **Data folder**, in this case `data=charts.example` means there is a file under `data/charts/example.yml`

  * Id: The id of the canvas, must be unique to use Chart.js

  * data: The data to pass to the chart constructor

    ```js
    new Chart(ctx, $chartData }});
    ```

    For example, the file `data/charts/example.yml` could contain the following data

    ```yaml
    type: "bar"
    data:
      labels: ['10-June-19', '11-June-19', '12-June-19', '13-June-19', '14-June-19', '15-June-19']
      datasets:
        - label: '# of Commits'
          data: [0, 24, 94, 21, 25, 34]
          backgroundColor: [
              'rgba(255, 99, 132, 0.2)',
              'rgba(54, 162, 235, 0.2)',
              'rgba(255, 206, 86, 0.2)',
              'rgba(75, 192, 192, 0.2)',
              'rgba(153, 102, 255, 0.2)',
              'rgba(255, 159, 64, 0.2)'
          ]
          borderColor: [
              'rgba(255, 99, 132, 1)',
              'rgba(54, 162, 235, 1)',
              'rgba(255, 206, 86, 1)',
              'rgba(75, 192, 192, 1)',
              'rgba(153, 102, 255, 1)',
              'rgba(255, 159, 64, 1)'
          ]
          borderWidth: 1
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
    ```

    



## Issues encountered

#### Posts not showing on the first page
* The page can not be in "profile mode"
* The files must be in the folder `content/posts/`
* There can not be any folder with file in `content/` that is alphabetically before `content/posts/`