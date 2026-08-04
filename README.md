# Lucid Inventory Tracker
Overview 

This automation tracks Lucid Air inventory from an investor’s perspective by collecting inventory data directly from Lucid’s website and monitoring how it changes over time. 

How it works

The automation uses Lucid’s inventory API to retrieve current vehicle listings. Each time the workflow runs, it performs three main tasks. 

1. Append History: Every Lucid Air in the current inventory is appended into the historical dataset, creating timestamped snapshots of inventory. As the automation runs daily at 6am, this builds a historical record that can be used to analyze sales and inventory data. 
2. Current Inventory: The current inventory sheet is cleared and repopulated everyday so it always reflects the latest inventory. 
3. Dashboard: Using the historical dataset, the dashboard calculates statistics that can help investors better understand inventory demand, supply, and pricing. 

The automation runs every day at 6am, and sends me a email to tell me it has run along with key summary statistics. 

Key Metrics Tracked

-Total in Inventory

-New Vehicles

-Disappeared/Sold Vehicles

-Revenue Last Day, Week, 90 days, Year

-Sold Last 7 days, Month, 90 days, Year

-New Inventory Last 7 days, Month, 90 days, Year

-Average and Median Price

-Average time to sell

-Inventory and Sales Week on Week and Month on Month Growth %


Limitations

The automation becomes more valuable as it collects more data. During the initial weeks, there will be missing data and the metrics will be based on a limited sample size so the data should be interpreted with caution. Additionally, as more data is collected and analyzed, it may become clear that other metrics will also be useful and should be utilized. Lastly, it only accounts for vehicles in inventory and can not account for custom orders. 

Next steps

Currently, the automation tracks only the Lucid Air. The next step is to add support for the Lucid Gravity while maintaining a separate dataset and dashboard. Since the two models target different segments of the market, combining their dashboards could obscure trends that are vehicle specific. 

Tech Stack

-n8n

-Google Sheets

-Lucid Inventory API
