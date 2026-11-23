# IS 455 · Winter 2027

Course worksheets and datasets for IS 455 at Brigham Young University. Links to each week's worksheets are posted on Canvas.

## Open a worksheet

Click the **Open in Colab** badge at the top of any worksheet, then choose **File → Save a copy in Drive** so your work is saved to your own Google Drive. Changes you make without saving a copy are lost when you close the tab.

## Datasets

Both datasets are synthetic and were created for this course. Neither contains real customers.

| File | Business | Rows | Data dictionary |
| --- | --- | --- | --- |
| `data/canyon_fitness_members.csv` | Canyon Fitness, a fictional chain of Utah gyms used in every A worksheet | 2,000 | [canyon_fitness_data_dictionary.md](data/canyon_fitness_data_dictionary.md) |
| `data/peakview_subscribers.csv` | Peakview Streaming, a fictional video-streaming service used in every B worksheet | 2,400 | [peakview_data_dictionary.md](data/peakview_data_dictionary.md) |

To load a dataset in Python, read its raw link with pandas.

```python
import pandas as pd
members = pd.read_csv("https://raw.githubusercontent.com/skous2/is455-w2027/main/data/canyon_fitness_members.csv")
```

## Worksheets

| Module | Worksheet A (optional prep, Canyon Fitness) | Worksheet B (required, Peakview Streaming) |
| --- | --- | --- |
| 1 · Jupyter and Python | [1A](module_01/Worksheet_1A_Jupyter_and_Python.ipynb) | [1B](module_01/Worksheet_1B_Jupyter_and_Python.ipynb) |
| 2 · pandas | [2A](module_02/Worksheet_2A_pandas.ipynb) | [2B](module_02/Worksheet_2B_pandas.ipynb) |
| 3 · Business understanding | [3A](module_03/Worksheet_3A_Business_Understanding.ipynb) | [3B](module_03/Worksheet_3B_Business_Understanding.ipynb) |
| 4 · Getting and cleaning data | [4A](module_04/Worksheet_4A_Getting_and_Cleaning_Data.ipynb) | [4B](module_04/Worksheet_4B_Getting_and_Cleaning_Data.ipynb) |
| 5 · Exploratory data analysis | [5A](module_05/Worksheet_5A_EDA.ipynb) | [5B](module_05/Worksheet_5B_EDA.ipynb) |
