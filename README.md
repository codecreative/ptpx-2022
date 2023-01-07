# ptpx-2022

Hello! Maybe you received one of my postcards for the pen plotter postcard exchange or possibly just a casual observer. Either way here is a little explanation about the concept and data behind the plot.


The pen plotter postcard exchange (ptpx) set up by [Paul](https://paulbutler.org/) is a fantastic initiative connecting people around the world over the joy of creating and sharing. Although I've been eyeing up a plotter for years I have only recently begun the journey so still new around these parts - this was great motivation, highly recommend!


## Concept and Background
Every 10 years after the census in the US, voting district lines are redrawn. In 2022, I had the fortunate position of [working on a project](https://www.cnn.com/interactive/2022/politics/us-redistricting/) with some incredibly kind and smart colleagues presenting what those new boundaries would look like and how the voters of the new district voted in the presidential election of 2020. 


This plot is a data visualization of the actual 2022 midterm election results of the US House of Representatives under those new districts. There are two versions of the plot

### Dark mode (red and blue) - Digital from Processing
![](https://github.com/codecreative/ptpx-2022/blob/main/dark-mode.png?raw=true)

### Light mode (pink and light blue) - Digital from Processing
![](https://github.com/codecreative/ptpx-2022/blob/main/light-mode.png?raw=true)


#### How to read
1. There are 435 districts, each square represents one district
2. The color of each square's lines represent the winning political party (Democrat = blue/light blue, Republican = red/pink)
3. The angle of the slope of the lines in the square match up to the margin of victory. A 2% margin of victory will be a fairly flat slope. A straight vertical line is a blow out of 90% margin (in some instances where there was no opponent it is actually 100% but I have allowed for a 90 max for visual purposes)
4. The space between the lines in a square varies to make each square lighter or darker so when viewed as a whole it gives the impression of the American flag. This is done by sampling a flag image for the location of each square in the grid and adjusting the line spacing.
5. The order is alphabetical by state from top left to bottom right. For example, Alabama has 7 districts starting in the top left (6 R and 1 D), Then Alaska's single district (D), Arizona and so on up to Wyoming's single district in the bottom right.


#### How it's made
1. Data from US House election results
2. Processing script, [borrowed heavily from this tutorial](https://sighack.com/post/cohen-sutherland-line-clipping-algorithm) to read data, draw the lines cropped within the squares.
3. The fantastic Python [vpype](https://vpype.readthedocs.io/en/latest/index.html) and [vsketch](https://vsketch.readthedocs.io/en/latest/) libraries to lay out to the postcard size, write on postcards, etc


#### The prints
![](https://github.com/codecreative/ptpx-2022/blob/main/the-plots.png?raw=true)
