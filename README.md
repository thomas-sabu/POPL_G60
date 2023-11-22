# POPL_G60

**Problem Statement**
- The aim is to conduct a comprehensive comparison of TensorFlow and PyTorch, exploring various facets, with the goal of assisting users in making informed decisions regarding the selection of the most suitable library for their individual projects.

- Has this been solved before?

While acknowledging that comparisons between TensorFlow and PyTorch have been conducted previously, our approach distinguishes itself by addressing a broader spectrum. Most existing analyses found online tend to concentrate on singular aspects, focusing solely on either model building or programming principles. Notably, the programming principles perspective has not received extensive research attention. In our project, we present a comprehensive report encompassing various aspects. Leveraging insights from the popl course, we emphasize differences between the libraries in critical areas such as determinism vs non-determinism, imperative vs declarative programming, dynamic vs static typing, functional vs object-oriented programming, and eager vs lazy evaluation. This enables users to make more informed decisions.


**Software Architecture**
- The software architecture involved in our solution revolves around deep learning frameworks, specifically PyTorch and TensorFlow/Keras, which are popular frameworks for building and training neural network models. Additional architectural aspects covered include their specific APIs, and the ways in which neural network models can be constructed and defined using these frameworks.
- The code is more concerned with the software architecture within the deep learning frameworks themselves, specifically PyTorch and TensorFlow/Keras, rather than dealing with a distributed system or client-server communication. Thus, our solution does not involve a client-server architecture.
- In our code, the testing component is executed locally. In brief, the testing phase involves evaluating the trained model on a separate dataset (in this case, the test set) to assess its performance on unseen data. 
- There is no explicit database involved.
- Given below is a diagram of one of the example neural networks we worked with, involving the Iris dataset. This multi-level perceptron gives a good general idea of the architecture of the networks we created. Of course, each node/neuron is connected to every other neuron in the previous and next layer. The connections have simply been omitted in the diagram for brevity.

![image](https://github.com/thomas-sabu/POPL_G60/assets/91559478/1e96b14f-6304-4c5e-9502-b4dca4f93e56)





**POPL Aspects**

In our comprehensive discussion within the POPL_Aspects.ipynb file, we delved into the foundational principles of programming perspectives. Our exploration encompassed the following key headings:

- Imperative vs Declarative Programming:
  This segment elucidated the distinctions and merits between imperative and declarative programming paradigms, shedding light on their respective strengths and applications.

- Dynamic vs Static Typing:
  Here, we navigated through the dynamic and static typing methodologies, elucidating their significance, advantages, and contexts where each excels.

- Functional vs Object-Oriented Programming:
  This section provided an insightful comparison between functional and object-oriented programming, highlighting their distinctive approaches, utility, and suitability in various scenarios.

- Eager vs Lazy Evaluation:
  Our discussion also delved into the nuances of eager and lazy evaluation strategies, expounding upon their operational differences and their impact on program execution.



**Results**
- PyTorch Training loop took considerably lesser time than Tensorflow training loops.


![image](https://github.com/thomas-sabu/POPL_G60/assets/91559478/debdcc0f-87b1-4a8b-b7c1-8b5c700247dc)

- TensorFlow training loop. (Eager Execution)
The default runtime of Tensorflow uses eager execution, which runs the lines of code immediately rather than building a computation graph to be run all at once.



![image](https://github.com/thomas-sabu/POPL_G60/assets/91559478/abc97959-b216-43ca-8b8c-eb011322a29e)


- TensorFlow training loop (Lazy execution)
This can be sped up by removing the model training logic into its own function and applying the @tf.function decorator, this allows the building of a computation graph that can be executed all at once resulting in massive speed gains.



![image](https://github.com/thomas-sabu/POPL_G60/assets/91559478/6475a693-359f-4421-8e5d-66067a8b3c87)






**Potential for Future Works**
- Our current project only compares PyTorch and tenserflow in the field of machine learning only using images as the dataset in the future we would use many different data sets to get a more accurate comparison between the two libraries. These may include:
1.	Text Data: Integrating natural language processing (NLP) capabilities into the project can involve working with text data. This could include tasks such as sentiment analysis, text classification, or language modeling. Comparing how PyTorch and TensorFlow handle the preprocessing, training, and deployment of models for text-related tasks would provide valuable insights for users working on applications involving textual information.
2.	Tabular Data: Many real-world machine learning applications involve structured tabular data, such as spreadsheets or databases. Expanding the project to include tabular data analysis would entail exploring how well PyTorch and TensorFlow handle tasks like regression, classification, and feature engineering on structured datasets. This is particularly relevant for applications in finance, healthcare, and business analytics.
3.	Time Series Data: Time series data is prevalent in fields such as finance, healthcare, and IoT. Future work in the project could involve evaluating the performance of PyTorch and TensorFlow in time series prediction tasks, anomaly detection, or forecasting. Handling temporal dependencies and understanding how well each framework supports recurrent neural networks (RNNs) or attention mechanisms would be crucial in this context.
4.	Audio Data: For applications involving sound, speech recognition, or music analysis, incorporating audio data into the project would be beneficial. Evaluating the frameworks' performance in tasks like speech-to-text or sound classification can provide users with insights into their suitability for audio-related machine learning applications.


Work Done by members:
1) POPL_Aspects -> Aditya Chatterjee
2) Model_types_building_training -> Thomas Sabu
3) Common_Errors,Misunderstandings -> Yash Lothe
4) Data_Types_and_data_handling -> Rohan Shroff






