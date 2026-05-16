# Notebooks

This folder contains Microsoft Fabric notebooks that complement the labs in [`../Instructions/Labs`](../Instructions/Labs). They are exported from Fabric in the standard `.ipynb` format and can be imported into any Fabric workspace.

## 📓 Notebook catalog

### `MedallionDemo_TransformDataFromBronzeSilverGold.ipynb`

A demonstration of the **medallion (Bronze / Silver / Gold)** lakehouse architecture in Microsoft Fabric. The notebook walks through:

- **🥉 Bronze** — landing raw source data into a lakehouse `Files` folder and registering an initial Delta table without transformation.
- **🥈 Silver** — cleansing, deduplicating, type-casting, and enriching the bronze data into conformed Delta tables suitable for analytics.
- **🥇 Gold** — modeling the silver data into business-ready dimension and fact tables that can be served to Power BI through the SQL endpoint.

**Pairs with:** [Lab 03b — Create a medallion architecture in a Microsoft Fabric lakehouse](../Instructions/Labs/03b-medallion-lakehouse-updated.md).

#### Prerequisites

- A Microsoft Fabric workspace with a **Lakehouse** attached (any name).
- A **trial, Premium, or Fabric capacity**.
- Basic familiarity with **PySpark** and **Spark SQL**.

#### Runtime

- Uses the default Fabric Spark runtime. Total execution time is typically **5–10 minutes** on a trial capacity once the Spark session has started.

## 🚀 How to import a notebook into Fabric

1. Download the `.ipynb` file from this folder (right-click → *Save link as…* on GitHub's *Raw* button).
2. In [Microsoft Fabric](https://app.fabric.microsoft.com), switch to the **Data Engineering** or **Data Science** experience.
3. Open your workspace and choose **New → Import notebook → Upload**, then select the downloaded `.ipynb` file.
4. Open the imported notebook and **attach a Lakehouse** using the *Lakehouses* pane on the left.
5. Run the cells top-to-bottom.

> 💡 If you only want to read along, GitHub renders `.ipynb` files directly in the browser — just click the file in this folder.

## 🤝 Contributing notebooks

When contributing a new notebook, please:

- **Clear outputs** before committing (`Cell → All Output → Clear` in Jupyter or *Run → Clear all outputs* in Fabric) so diffs stay small and the repo doesn't bloat.
- Add a **header markdown cell** at the top with: title, learning objectives, prerequisites, and the lab(s) it pairs with.
- Use **markdown cells between code blocks** to explain *why*, not just *what*.
- Add an entry to the **Notebook catalog** above describing the notebook and the lab it pairs with.
