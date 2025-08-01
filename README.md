# Data Scientist (Academic Project) – Time Series Prediction with Recurrent Networks (RNN)

## Climate Data Modeling with R, TensorFlow, and Keras 3

I set myself the challenge of forecasting future temperatures based on historical data, using the complex Jena climate dataset. My goal was to apply and compare different neural network architectures to a time series problem, demonstrating a methodical approach to moving from a simple solution to a more sophisticated and effective one.
The first step was rigorous data preprocessing. I normalized the entire dataset and, most importantly, designed and built a custom data generator in R. This feature was crucial for handling the large volume of data efficiently, creating batches of temporal sequences (the last 10 days of data) and their corresponding targets (the temperature 24 hours in the future) on the fly, an essential technique for training Deep Learning models with sequential data.

My modeling strategy was deliberately iterative to demonstrate a process of continuous improvement:
1. Baseline: First, I established a common-sense benchmark, predicting that the future temperature would be equal to the current temperature. This gave me a baseline Mean Absolute Error (MAE) that any more complex model had to surpass to be considered useful.
2. Basic Dense Model: My first attempt at Deep Learning was a simple dense neural network. Although it slightly outperformed the baseline, its performance was limited, as this architecture is not designed to interpret the temporal order of the data.
3. Introduction of Recurrent Networks (GRU): To capture the sequential nature of the problem, I implemented a model with a GRU (Gated Recurrent Unit) layer. This model, by having memory of the previous steps, achieved a significant improvement in performance, far outperforming the previous two approaches.
4. Optimization and Improvement: To build a truly robust model, I attacked the overfitting problem by adding Dropout and Recurrent Dropout regularization.

Additionally, I explored deeper architectures, such as stacking multiple GRU layers, and finally, I implemented a Bidirectional GRU model, which allows the network to learn patterns from both past and future sequences.
Each step in this process represented a measurable improvement over the previous one, culminating in a Bidirectional Recurrent Model that proved to be the most effective solution for this forecasting problem.

Demonstrated Achievements and Skills:
+ Developed a predictive model for time series, successfully forecasting future temperature from multivariate climate data.
+ Systematically implemented and compared multiple neural network architectures, including dense models, GRUs, stacked GRUs, and bidirectional GRUs, demonstrating extensive knowledge of deep learning tools for sequences.
+ Established a rigorous benchmark with a baseline model, a fundamental practice for objectively evaluating the performance of complex models.
+ Built a custom and efficient data generator in R to handle large sequential datasets, a key technical skill in deep learning projects.
+ Applied advanced techniques to combat overfitting, such as Dropout and Recurrent Dropout, demonstrating a practical understanding of the challenges of training RNNs.
+ I demonstrated a methodical and iterative approach to model improvement, starting with a simple solution and adding justifiable complexity at each step to improve performance.
