# [Anomaly Detection](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-anomaly-detection)
Anomaly detection is an AI feature that helps you enhance your line charts by automatically detecting anomalies in your time series data. This is found in the Analytics Pane > Find Anomalies.

You can only use this when _one_ field is in the value well, and when forecasting is not applied.

<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156252651-d696d3f0-cfac-4f05-ac73-5986138ccda5.gif" width=600/></p>

The experience his highly customizable. Users can format the anomaly's shape, size, and color, and also the color, style, and transparency of expected range. You can also configure the parameter of the algorithm. If you increase the sensitivity, the algorithm is more sensitive to changes in your data. In that case, even a slight deviation is marked as an anomaly. If you decrease the sensitivity, the algorithm is more selective on what it considers an anomaly.

### Explanations
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156253270-36788a25-dc1a-467b-ac16-9b8e7abfe612.gif" width=600/></p>

Use `Explain By` to force PBI to try and explain anomalies by a given field:
<p align="center"><img src="https://user-images.githubusercontent.com/29554021/156253514-53eb063b-0ac7-4b45-bd02-8e9444b3e45b.png" width=600/></p>
