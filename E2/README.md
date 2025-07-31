# Recording Evaluation Dataset Convergence

This repository contains the evaluation dataset used to assess the convergence and coverage of the SPSS Modeler Q\&A knowledge base. It includes the following source documents:

* `dataview.html`
* `flow_scripting.html`
* `getting-started.html`
* `migration.html`
* `flow_scripting_example.html`
* `flow_properties.html`
* `models-overview.html`
* `parameters.html`
* `save_model.html`


---

## Evaluation Set, Total evaluation items: 9
```json
[
  {
    "question": "Which two methods can you use to visualize data in SPSS Modeler: one inside a flow using a specific node, and another via an external service mentioned in the documentation?",
    "correct_answer": "Use a Charts node to open the chart builder within a flow, and use the Data Refinery service to visualize your data externally.",
    "correct_answer_document_ids": [
      "dataview.html"
    ]
  },
  {
    "question": "How do you access scripting in a SPSS Modeler flow and what scripting language is used by default?",
    "correct_answer": "Click the Scripting option in the flow’s properties toolbar to open the script editor, and Python is the default scripting language.",
    "correct_answer_document_ids": [
      "flow_scripting.html"
    ]
  },
  {
    "question": "What video platforms are used for the SPSS Modeler introduction tutorial and the flow import migration guide?",
    "correct_answer": "The introduction tutorial uses the IBM video platform (video.ibm.com), and the import migration guide uses Ustream (ustream.tv).",
    "correct_answer_document_ids": [
      "getting-started.html"
    ]
  },
  {
    "question": "What file extension is used for SPSS Modeler streams and which flow property option enables behind-the-scenes node reordering for performance optimization?",
    "correct_answer": "Streams use the `.str` file extension, and the “Enable flow rewriting” option automatically reorders nodes for optimization.",
    "correct_answer_document_ids": [
      "migration.html"
    ]
  },
  {
    "question": "In the flow scripting example, what method is used to link a model apply node to an analysis node, and where do you specify that the script runs when the flow runs?",
    "correct_answer": "The method `stream.linkBetween(appliernode, typenode, analysisnode)` links the nodes, and you select “Run the script” in the Scripting tab of the flow properties to have it execute each time the flow runs.",
    "correct_answer_document_ids": [
      "flow_scripting_example.html"
    ]
  },
  {
    "question": "How do you define parameters in SPSS Modeler flows and how can you access the flow scripting editor to customize operations within a flow?",
    "correct_answer": "You define parameters by opening Flow properties and clicking Add value to set parameters available to all nodes; you access the scripting editor by clicking Scripting in the flow’s toolbar.",
    "correct_answer_document_ids": [
      "flow_properties.html"
    ]
  },
  {
    "question": "What is a flow and what is a node in SPSS Modeler?",
    "correct_answer": "A flow is a sequence of data-processing operations representing the path of your data; a node is a modular, self-contained operation represented graphically by a unique icon.",
    "correct_answer_document_ids": [
      "models-overview.html"
    ]
  },
  {
    "question": "How do you define parameters for flows and what distinguishes flow parameters from local script variables?",
    "correct_answer": "You define parameters in Flow properties or in a flow script; flow parameters are saved with the flow and available to all nodes, whereas local script variables exist only within the script in which they’re declared.",
    "correct_answer_document_ids": [
      "parameters.html"
    ]
  },
  {
    "question": "What are three benefits of deploying SPSS Modeler models to watsonx.ai Runtime?",
    "correct_answer": "Real-time insights for faster decision-making, scalability to handle growing data and demand, and integration via API endpoints into other systems and applications.",
    "correct_answer_document_ids": [
      "save_model.html"
    ]
  }
]
```
###  Sample Questions for 'flow_properties.html'

1. **Question:** What property controls how many rows are shown when you preview data for a node?  
   **Answer:**  
   > **Maximum number of rows to show in Data Preview**  
   > When you preview the data for a node, you can specify the number of rows to show.

2. **Question:** How does SPSS Modeler handle nominal (set) fields when they exceed a certain number of members?  
   **Answer:**  
   > **Limit members for nominal fields**  
   > The data type of the nominal (set) fields becomes Typeless when the number of members exceeds the maximum number of members that you set in Maximum members. This option is useful when you are working with large nominal fields. When the measurement level of a field is set to Typeless, its role is automatically set to None. Fields that are set to None aren't available for modeling.

3. **Question:** Which setting lets you import timestamps measured in microseconds?  
   **Answer:**  
   > **Use microseconds in timestamp fields**  
   > If you have timestamp data that is measured in microseconds, you can enable this option to use the more precise data in your flows. To enable the option, select this checkbox and String for the Import date/time/timestamp as setting.  
   > **Note:** This option works only for connectors that support SQL pushback.

4. **Question:** What does the “Optimize CLEM expressions” option do?  
   **Answer:**  
   > **Optimize CLEM expressions**  
   > This option enables the optimizer to search for CLEM expressions that can be preprocessed before the flow runs to increase the processing speed. For example, if you have an expression such as `log(salary)`, the optimizer calculates the actual salary value and passes that on for processing. This option can be used to improve both SQL pushback and SPSS Modeler performance.

###  Sample Questions for 'flow_scripting_example.html'

1. **Question:** What does the first line `stream = modeler.script.stream()` do in the flow scripting example?  
   **Answer:**  
   > It defines a variable that points to the current flow.

2. **Question:** How does the script find the Neural Network builder node?  
   **Answer:**  
   > By calling `stream.findByType("neuralnetwork", None)`.

3. **Question:** What is the purpose of the `results = []` line in the script?  
   **Answer:**  
   > It creates a list where the execution results can be stored.
