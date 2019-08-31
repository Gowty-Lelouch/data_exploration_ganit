Understanding the data

file_01 : Contains information of the product quantities that needs to be supplied from source facility location to customer location and who is the current logistics vendor to fulfill the supply

file_02: Have the cost (per product) data that needs to be paid to each logistics vendor (as per the product size etc etc)

file_04: Has the information about the zones (which source_facility and customer location combination falls into which zone)

Questions to be answered

What is the current vendor wise supply volume distributed
What is the current vendor wise cost incurred for fulfilling the supply network
What is the least cost that will be incurred to fulfill this supply network?
How much cost savings can be done if we chose the least cost to fulfill this network
The process flow for the solution. Please find attached an illustrative example.
Bonus question (Optional) – Descriptive and data interpretation

You are to give a presentation about your supply network to the new CXO that has just joined. Highlight some of the facts that he will be interested to know. For example:
Which is the busiest zone
Who is my most economical vendor




# Sample Codes

# Groupby Vendor, Payment Mode, and shipment size, and sum them to find all possible values

gdf = info_df.groupby(by=['current_logistics_vendor', 'payment_option', 'shipment_size'], as_index=True).sum()
gdf