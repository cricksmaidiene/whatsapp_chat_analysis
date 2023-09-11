# Exploratory WhatsApp Chat Analysis

- [Exploratory WhatsApp Chat Analysis](#exploratory-whatsapp-chat-analysis)
  - [About 💁🏻‍♀️](#about-️)
  - [Gallery 📸](#gallery-)
  - [Setting Up 🛠️](#setting-up-️)
  - [Executing the Notebook 📝](#executing-the-notebook-)
  - [Flow of Execution 📊](#flow-of-execution-)
  
![](https://img.shields.io/badge/WhatsApp-25D366.svg?style=for-the-badge&logo=WhatsApp&logoColor=white)
![](https://img.shields.io/badge/Android-3DDC84.svg?style=for-the-badge&logo=Android&logoColor=white)
![](https://img.shields.io/badge/iOS-000000.svg?style=for-the-badge&logo=iOS&logoColor=white)

![](https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)
![](https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=Python&logoColor=white)
![](https://img.shields.io/badge/pandas-150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![](https://img.shields.io/badge/Plotly-3F4F75.svg?style=for-the-badge&logo=Plotly&logoColor=white)

## About 💁🏻‍♀️

- **Privacy-centric Analysis:** Securely review summaries of WhatsApp conversations, whether with individuals or group chats.
- **Local Processing:** Data never leaves the executing system. Analysis is carried out entirely locally, ensuring utmost privacy.
- **Transparent Code Execution:** Jupyter notebooks are utilized to provide full transparency. Users can inspect every line of code that processes chat data. After insights are generated, all chat data is immediately purged from memory.
- **In-depth Metrics:** Delve into chat data. Load conversations and uncover insights such as response times, text density, emoji usage, and more.

## Gallery 📸

<img src="assets/newplot.png" width="400px">
<img src="assets/density.png" width="400px">
<img src="assets/response_time.png" width="400px">
<img src="assets/messages.png" width="400px">

## Setting Up 🛠️

- Recreate conda environment using the following

```bash
git clone https://github.com/cricksmaidiene/whatsapp_chat_analysis.git
cd whatsapp_chat_analysis
conda create --name whatsapp_chat_analysis --file env.txt
conda activate whatsapp_chat_analysis
```

Then run either:

```
jupyter lab
```

or

```
jupyter notebook
```

Either of the following are the jupyter requirements & versions:

- `jupyterlab==2.2.6` requires `jupyter labextension install jupyterlab-plotly@4.14.3`, in turn requires `nodejs >= 10.0`. Install nodejs with `conda install nodejs -c conda-forge --repodata-fn=repodata.json`
- `jupyter notebook==6.2.0`

## Executing the Notebook 📝

- To export a WhatsApp chat as a `txt` file in either iOS or Android, go to a particular chat with a person or group and check the options. There is an option to export chat. Select `Without Media` and save the resulting text file in the same directory as the notebook.
- Modify the second cell of the notebook with the chat `txt` filename / filepath. This highlights to the notebook on which chat file is to be analyzed.
- Run all cells

## Flow of Execution 📊

- Text file is loaded, cleaned up and parsed. The messages are turned into a table (or dataframe) at a per-message level.
- Once the dataframe is created, it is aggregated and re-aggregated for different analyses and visualized using plotly express.
