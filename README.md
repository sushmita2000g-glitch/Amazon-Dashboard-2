# Amazon Sales Intelligence Dashboard

A fully dynamic, single-file sales analytics dashboard built with HTML, CSS, and JavaScript. It visualizes Amazon sales data across revenue, orders, customers, product performance, regional breakdown, and conversion funnel — all rendered in the browser with no backend required.

## Overview

This project is a Power BI-style business intelligence dashboard designed for Amazon sales data. It is built as a single standalone HTML file and runs entirely in the browser. All charts, tables, animations, and real-time simulations are powered by Chart.js and vanilla JavaScript with no frameworks or build tools required.

The dashboard was designed to closely resemble a professional BI tool with a dark theme, animated KPI cards, a live ticker, interactive chart toggles, sortable data tables, and a simulated real-time data feed that updates every 2.5 seconds.\


## Features

The dashboard is organized into five main rows of visual components.

The top row contains five KPI cards covering Total Revenue, Total Orders, Active Customers, Average Order Value, and Return Rate. Each card animates from zero to its final value on load and includes a small sparkline trend chart.

The second row contains a monthly Revenue vs Budget bar chart for the full year 2024 with a toggle to switch between bar and line view, a doughnut chart showing sales breakdown by channel (Amazon.in, Amazon.com, Amazon.co.uk, and Other), and a horizontal bar chart of the top eight product categories by units sold.

The third row contains a sortable product table showing the top eight products with revenue, units, and margin columns, a region performance panel with animated progress bars and a bar chart for South Asia, North America, Europe, and Asia Pacific, and a performance score ring with six supporting metrics including conversion rate, fulfillment rate, and NPS score.

The fourth row contains a sales funnel showing the conversion flow from impressions down to purchases alongside a conversion trend line chart, a category heatmap showing GMV distribution across nine categories with heat-based color intensity, and an hourly orders bar chart that simulates real-time updates every 2.5 seconds with peak hours highlighted.

The fifth row contains a weekly revenue trend comparing 2024 and 2023 over eight weeks, a top sellers leaderboard table showing GMV and ratings for six sellers, and a polar area chart showing the split between Prime, Non-Prime, Business, and Pantry orders.

A sticky header at the top includes the Amazon logo, a live clock, date range filter buttons, and a live status badge. A scrolling ticker below the header displays ten live metrics including stock price, revenue, conversion rate, and delivery time.


## Tech Stack

The dashboard uses only three technologies. HTML5 provides all structure and layout. CSS3 handles all styling including CSS custom properties for theming, grid layout for all five rows, keyframe animations for the ticker and live dot, and smooth transitions on hover and filter interactions. JavaScript handles all data definitions, chart rendering via Chart.js 4.4.1, animated value counting, real-time data simulation, table sorting, and the live clock.

Chart.js is loaded from the Cloudflare CDN. Google Fonts loads Rajdhani and JetBrains Mono. No other external dependencies exist.


## File Structure

The entire project is a single file.


amazon-sales-dashboard/
    amazon_sales_dashboard.html
    README.md


There are no dependencies to install, no build steps, and no configuration files.

## Getting Started

To run the dashboard locally, clone the repository and open the HTML file directly in any modern browser.


git clone https://github.com/your-username/amazon-sales-dashboard.git
cd amazon-sales-dashboard


Then open `amazon_sales_dashboard.html` in Chrome, Firefox, Edge, or Safari. An internet connection is required on first load to fetch Chart.js from the CDN and load the Google Fonts. After the initial load, all rendering happens locally.

To host it on GitHub Pages, go to the repository settings, navigate to the Pages section, set the source branch to main, and set the folder to root. The dashboard will be live at `https://your-username.github.io/amazon-sales-dashboard/amazon_sales_dashboard.html`.


## Data

All data in this dashboard is static and defined directly in the JavaScript section of the HTML file. It represents a sample Amazon seller dataset for the year 2024 including twelve months of revenue and budget figures, channel breakdown percentages, category unit sales, eight product records with revenue, units, and margin, four regional performance records, a five-stage sales funnel, nine heatmap categories, hourly order distribution across 24 hours, eight weeks of revenue trend data comparing 2024 and 2023, six seller leaderboard records, and prime membership split percentages.

To use real data, replace the values in the data section at the top of the script block. All arrays and objects are clearly labeled with comments. No schema changes are required as long as the array lengths and object keys remain consistent.


## Customization

The color scheme is controlled entirely through CSS custom properties defined in the `:root` block at the top of the style section. Changing `--or` updates the primary orange accent used across all charts, borders, and highlights. The dark background colors, text colors, and border colors can all be adjusted independently.

Chart colors are defined as arrays at the top of the script block and can be changed independently of the theme variables.

The real-time update interval is set to 2500 milliseconds and can be adjusted by changing the value in the `setInterval` call near the bottom of the script.


## Browser Compatibility

The dashboard works in all modern browsers. It has been tested in Chrome 120, Firefox 121, Edge 120, and Safari 17. It does not support Internet Explorer.


## Author

Sushmita Poddar
BCA Graduate, IGNOU Delhi
Data Analyst and Data Scientist
Portfolio: GitHub Pages
LinkedIn: linkedin.com/in/sushmita-poddar

## License

This project is open source and available under the MIT License.

MIT License

Copyright (c) 2024 Sushmita Poddar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
