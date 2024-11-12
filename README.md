# PowerBI-AdventureWorks-Purchassing-Analysis
## Project overview 
This project presents a comprehensive Power BI dashboard analyzing the purchasing operations of AdventureWorks Cycles, a fictitious bicycle manufacturer. The dashboard is designed to provide executive leadership with actionable insights into procurement efficiency, supplier performance, and inventory management.
## Bussiness context
AdventureWorks Cycles requires efficient purchasing operations to maintain optimal inventory levels for manufacturing their bicycle products. The purchasing department faces several key challenges:
- Ensuring adequate stock levels for production demands
- Meeting delivery timelines
- Optimizing procurement costs
- Managing supplier relationships
- Maintaining quality standards
## Dataset 
The analysis utilizes the AdventureWorks sample database:
- Dataset: AdventureWorks2019 (public Google BigQuery dataset)
- Dataset dictionary: Available at https://drive.google.com/file/d/1oYm32cdutBwHhkds4l-HznDYPZ5_WCxu/view↩
- Data schema: Available at  https://i0.wp.com/improveandrepeat.com/wp-content/uploads/2018/12/AdvWorksOLTPSchemaVisio.png?ssl=1↩
##  Technical Implementation
- Power BI for Visualization: Design dashboards to display key insights visually, using charts, tables, and KPIs.
- Data Processing: Use Power Query to clean and transform data, and structure a well-designed data model.
- Dynamic Filters: Set up dynamic filters to allow leadership to easily select suppliers, products, or time frames.
- Calculations and Measures: Use DAX to create measures such as total cost, average order time, and optimal stock levels.
## Design Thinking Steps 
### Stage 1 - Empathy 
![image](https://github.com/user-attachments/assets/393683de-feee-443c-a56c-c8655b58aece)
### Stage 2 - Define 

#### Stage 3: Ideate 
<table>
  <thead>
    <tr>
      <th>Idea Name</th>
      <th>Layer 0 Dimension: Overall Metrics</th>
      <th>Layer 1 Dimension: Metrics Breakdown</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4">Vendor Performance</td>
      <td rowspan="4">OTIF Rate (Includes breakdowns)</td>
      <td>OTIF Rate by ActiveFlag</td>
    </tr>
    <tr>
      <td>OTIF Rate by CreditRating</td>
    </tr>
    <tr>
      <td>OTIF Rate by PreferredVendorStatus</td>
    </tr>
    <tr>
      <td>Related Metrics</td>
    </tr>
    <tr>
      <td rowspan="4">Cost Efficiency</td>
      <td rowspan="4">Price - Quality Rate (Includes breakdowns)</td>
      <td>Price - Quality Rate by ActiveFlag</td>
    </tr>
    <tr>
      <td>Price - Quality Rate by CreditRating</td>
    </tr>
    <tr>
      <td>Price - Quality Rate by PreferredVendorStatus</td>
    </tr>
    <tr>
      <td>Related Metrics</td>
    </tr>
  </tbody>
</table>

#### Stage 4: Prototype and Review
Next, I proceeded with Step 4 - Prototype and Review multiple times and achieved the final result, which will be presented in the following section as a dashboard.
## DashBoard 
### Data Modeling 
![image](https://github.com/user-attachments/assets/f2c5c56b-9036-4e62-96ba-1f55f9df6731)
### View 1: Vendor Performance 
![image](https://github.com/user-attachments/assets/d57baa99-2a6b-47c1-8f56-9deb769979ae)
### View 2: Cost Efficiency 
![image](https://github.com/user-attachments/assets/62dcce51-0c8d-4836-9c4f-06befae026d2)
## Insight & Recommendation
### Vendor Performance 
#### Analysis
The "Vendor Performance" table evaluates the overall performance of suppliers based on several key metrics, such as the On-Time and In-Full (OTIF) rate, average shortage rate, and order rejection rate.
- OTIF Rate: This rate stands at 95.6%, reflecting a high capability of suppliers to meet order requirements on time and in full. However, there is a clear discrepancy between suppliers, indicating the need for adjustments or improvements for some suppliers.
- Average Shortage Rate: At 11.57, this rate suggests that demand forecasting and current inventory management may need improvement to avoid product shortages.
- Order Rejection Rate: This rate is at 6.37, indicating a significant portion of orders are rejected, affecting production processes and customer satisfaction.
#### Recommendations
- Enhance collaboration and performance management with suppliers: Although the overall OTIF rate is 95.6%, it is essential to establish regular performance evaluation meetings with suppliers who have lower rates to understand the issues and support them in improving. These issues may relate to logistics, production, or financial factors. Implement training programs, guidance, or process improvements to enhance performance.
- Improve demand forecasting and inventory management processes: The high shortage rate indicates inaccuracies in demand forecasting. Modern forecasting models, such as Machine Learning, should be utilized to improve accuracy in demand forecasting and inventory management. This will help minimize shortages and ensure products are always available for delivery.
- Analyze causes and reduce the order rejection rate: With the order rejection rate at 6.37, it is crucial to analyze the underlying causes leading to this situation. It could be due to product quality, order processing procedures, or unclear requirements. Implement corrective solutions such as improving quality control processes, enhancing order processing systems, and better communication with suppliers.
- Focus on collaboration with suppliers with high credit ratings and appropriate preferred vendor status: Suppliers with high Credit Ratings (2) and good Preferred Vendor Status show the highest performance in meeting requirements. The company should build long-term collaboration plans with these suppliers and reassess those that do not meet requirements to improve or adjust collaboration strategies.
### Cost Efficiency
#### Analysis
The "Cost Efficiency" table provides an overview of cost efficiency related to product price and quality, total cost of ownership, and the effectiveness of volume discounts.
- Price-Quality Rate: This index measures the ratio of product quality (determined by the rejection rate versus received products) to the average product price. At 0.03, it indicates that the quality of products received compared to the cost incurred is at an average level.
- Total Cost of Ownership: This index is at 1.08, indicating that the total costs, including product price, shipping fees, and taxes, are 8% higher than the average product price. This suggests that ancillary costs are significantly impacting total ownership costs.
- Volume Discount Effectiveness: The index of -18.86% shows that purchasing in bulk has helped reduce the average price by 18.86% compared to the overall average price. This means that the discount strategy is generally effective.
#### Recommendations
- Renegotiate with suppliers with lower credit ratings: Suppliers with the highest credit rating (CreditRating = 5) are providing products with the highest Price-Quality Rate (0.042). A high Price-Quality Rate may correspond to higher product prices with quality matching the price. However, to optimize costs, the company can consider collaborating with suppliers with lower credit ratings but who can still provide stable quality products. The goal is to find suppliers who can deliver quality products at lower prices, thus reducing overall costs without compromising product quality.
- Optimize ancillary costs such as shipping and taxes: With a Total Cost of Ownership Index of 1.08, it is necessary to review shipping processes and collaborate with logistics partners to renegotiate rates or change partners if necessary. Additionally, optimizing shipping plans, such as consolidating shipments or optimizing the quantity of goods per trip, can help reduce shipping costs and improve this index.
- Encourage larger volume purchases: The current Volume Discount Effectiveness index indicates that purchasing in bulk is providing significant cost benefits. Therefore, departments should be encouraged to purchase larger quantities or negotiate with suppliers to adjust discount thresholds, thereby enhancing the effectiveness of promotional and discount programs.
### Conclusion
Improving cost efficiency and supplier performance requires a comprehensive approach, including renegotiating prices, optimizing costs, improving supply chain management, and collaborating closely with capable suppliers. Implementing these strategies will not only help the company save costs but also enhance operational efficiency and customer satisfaction.


