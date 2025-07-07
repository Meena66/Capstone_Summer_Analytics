# Capstone_Summer_Analytics
This project implements a real-time dynamic pricing model for smart parking using the Pathway stream processing engine. It simulates live data from multiple parking lots and calculates hourly parking prices based on occupancy, traffic conditions, queue lengths, vehicle types, and other demand factors.

#Tech Stack
Python
Pathway
Pandas
Bokeh and Panel (for real-time visualization)
Google Colab (for development)

#Project Workflow
1.The parking dataset is streamed using Pathway.replay_csv().
2.Data is grouped into 1-hour tumbling windows.
3.Features like occupancy, traffic, and queue length are aggregated.
4.A custom dynamic pricing formula calculates hourly rates.
5.Prices are visualized in real time using Bokeh and Panel.

#Pricing Formula
price = base_price * (1 + λ * normalized_demand)
Demand score is based on:
Occupancy-to-capacity ratio
Queue length
Traffic score
Vehicle type weight
Special day flag
Final price is clipped between a minimum (₹5) and maximum (₹20).

#Architecture Flow


![architecture mmd](https://github.com/user-attachments/assets/5564f66d-131f-4fe4-8a5b-f93a4360d12e)
![image](https://github.com/user-attachments/assets/a6df0800-c570-4ad4-b7f5-3cc954a4e7e6)


#Important Links
Google Colab Notebook
Pathway GitHub Repository
LLM App GitHub Repository
