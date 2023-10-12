# Adding tables easily to this site
Pranav Kumar Mishra
Thursday, October 12, 2023

To easily interchange between the formats, paste your table into
<https://tablesgenerator.com/markdown_tables>

## Markdown

The easiest way to add tables into a `.qmd` file is to add it as a
markdown formatted table. Here is an example from w3schools:

    |Header1 |Header2  | Header3|
    --- | --- | ---|
    |data1|data2|data3|
    |data11|data12|data13|

### Output

| Header1 | Header2 | Header3 |
|---------|---------|---------|
| data1   | data2   | data3   |
| data11  | data12  | data13  |

## HTML with CSS

You can also place the same table using HTML

``` html
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky">Header1</th>
    <th class="tg-0pky">Header2</th>
    <th class="tg-0pky">Header3</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">data1</td>
    <td class="tg-0pky">data2</td>
    <td class="tg-0pky">data3</td>
  </tr>
  <tr>
    <td class="tg-0pky">data11</td>
    <td class="tg-0pky">data12</td>
    <td class="tg-0pky">data13</td>
  </tr>
</tbody>
</table>
```

### Output

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>

| Header1 | Header2 | Header3 |
|---------|---------|---------|
| data1   | data2   | data3   |
| data11  | data12  | data13  |
