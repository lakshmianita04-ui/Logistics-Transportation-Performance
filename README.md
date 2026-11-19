# Logistics-Transportation-Performance
Solution 

● Trip ID, Vehicle ID, Driver ID, Origin, Destination, Distance (km), Fuel Consumed(liters), Delivery Status (On-Time/Late), Delivery Date.
Trip ID column changed and added IDs. 

● Vehicle Master: Vehicle ID, Vehicle Type, Capacity, Maintenance Cost.
No changes.

Data Cleaning Modeling: (5marks)
○ Fix missing fuel consumption values (use avg. per vehicle type).
In Power BI, select reference and select Group By  using Trip ID . Create a column named  Avg Fuel Consumption, and avg  and select fuel consumed 

○ Relate Trips with Vehicle Master.
Merge Trips with Vehicle Master using merge queries  by trip ID.

DAX Measures: (5marks)

○ Fuel Efficiency = Distance / Fuel Consumed
Fuel Efficiency = DIVIDE(SUM('Trip Data'[Distance_km]),SUM('Trip Data'[Fuel_Consumed_L]))

○ On-Time Delivery % = On-Time Trips / Total Trips
On-Time Delivery = (30/50)*100 On-Time Trips=30
Total Trips=50
○ Cost per km = (Fuel Cost + Maintenance Cost) / Distance
Cost per Km = DIVIDE(SUM('Trip Data'[Fuel Cost])+SUM('Trip Data'[Fuel_Consumed_L]),SUM('Trip Data'[Distance_km]))
