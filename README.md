## Dataset

The following table shows a sample of the dataset collected through the **SmartWMS** system. Each row represents an individual picking task, with various attributes related to the picking process.

| Article                                                          | Quantity | Picking Location                                                 | Previous Location                                                | Pick | Distance (m) | Total Duration (s) | Walking Duration (s) | Picking Duration (s) |
| ---------------------------------------------------------------- | -------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---- | ------------ | ------------------ | -------------------- | -------------------- |
| 84b2476222e2936db72bbb6aa7c6ede17e4da7adcb2e527ee368ca00692a8301 | 12       | d22c652909bc987c94c01e9255e354088465d1b355ca5a1021240a7bd7d703a0 | bcbf640c8eacde6dd567dbdff0c854f250f9d8597d912a0efdab74e396190160 | true | 20           | 32                 | 14.71                | 17.29                |
| 84b2476222e2936db72bbb6aa7c6ede17e4da7adcb2e527ee368ca00692a8301 | 12       | d22c652909bc987c94c01e9255e354088465d1b355ca5a1021240a7bd7d703a0 | f5cae135a5e5dbc1d28ac721996788fe557c56cfcd3d317c9b568f0924843e4f | true | 13.828       | 35                 | 10.17                | 24.83                |
| 84b2476222e2936db72bbb6aa7c6ede17e4da7adcb2e527ee368ca00692a8301 | 12       | d22c652909bc987c94c01e9255e354088465d1b355ca5a1021240a7bd7d703a0 | 84e929e2b17ee12df113f2cc0f8935843338d0c9aec036eb6247e597527cd6ed | true | 22.61        | 126                | 16.62                | 109.38               |

### Attribute Descriptions:
- **Article**: The unique identifier of the article (product) being picked.
- **Quantity**: The number of items to be picked.
- **Picking Location**: The unique identifier for the location from which the item is being picked.
- **Previous Location**: The location from which the picker previously picked an item, used for calculating travel distances.
- **Pick**: A boolean indicator that shows whether the location is a picking location (`true`) or a stock location (`false`).
- **Distance (m)**: The distance, in meters, traveled between picking locations.
- **Total Duration (s)**: The total time taken for the picking, including walking and picking.
- **Walking Duration (s)**: The time spent walking between locations during the picking.
- **Picking Duration (s)**: The time spent actually picking the item from the location.


## ⚠️ Note on Encoded Data

This dataset includes encoded values for certain fields, such as article and location identifiers. These values represent internal database primary keys and have been intentionally obfuscated to protect data confidentiality. The dataset is derived from production systems containing real-world operational data, and the encoding ensures that no sensitive or proprietary information is exposed.

The encoded identifiers remain consistent across the dataset and can be safely used as categorical keys. However, they do not convey semantic meaning. 
> **Important:** No descriptive information about articles—such as names, dimensions (gabarits), or other identifying attributes—is included in this dataset.
