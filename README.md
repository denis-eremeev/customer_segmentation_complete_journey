# customer_segmentation_complete_journey
Example of customer segmentation based on The Complete Journey open dataset ( https://www.kaggle.com/frtgnn/dunnhumby-the-complete-journey ) and dashboard built on top with Python libs: plotly and voila (optional, for rendering)
This repository comprises 3 Jupyter notebooks and input (partly) / output text files:
  1) segmentation.ipynb
    inputs: {transaction_data, product, hh_demographic}.csv (not presented, see link above)
    outputs: {output_kmeans_labels, output_kmeans_centers}.csv
    This doing kmeans clustering of households based on its purchases data represented as normalized vector in n+4-dimensional space, where n - number of purchases' category (DEPARTMENT). Besides category split of purcases', categorized time of transaction is used (morning, day, evening, night).
   2) Segment description.csv - text file build manually based on output_kmeans_centers.csv
   3) dashboard.ipynb
    inputs: {transaction_data, product, output_kmeans_labels, Segment description}.csv
    outputs: plotly interactive charts
    This produces descriptive analytics based on segmentation results: dynamic of households' number within a cluster, their spendings compared to all spendings, cluster growth within a previous year, its comparison with other cluster perfomance. User can select number of cluster and deparments or select all of them. Voila package may be used to render plotly to web page.
   4) data_chart1.csv - dataset for dashboard made from The Complete Journey dataset.
   5) dashboard_light.ipynb
      The same as dashboard with inputs: {data_chart1, Segment description}.csv
