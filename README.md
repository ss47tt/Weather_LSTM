# Weather_LSTM

How to do training, validating, and testing on weather dataset?

1. Download the dataset at https://paperswithcode.com/dataset/weather-ltsf or https://drive.google.com/file/d/1Tc7GeVN7DLEl-RAs-JVwG9yFMf--S8dy/view?usp=share_link

2. In the weather dataset, there are date column and 21 feature columns.

3. The data are of 10 second intervals from 1/1/2020 0:10 to 1/1/2021 0:00 with 52696 rows of data.

4. I split the dataset into train : validate : test ratio of 7 : 2 : 1 = 36803 : 10515 : 5258.

5. The input sequence length is 96 = 960 minutes = 16 hours.

6. The output target sequence length is 24 = 240 minutes = 4 hours.

7. I also did the training, validating, and testing with sliding window.

   The window length = length of data - input length - output length.

   For the case of training data, the window length of the training data = 36803 - 96 - 24 = 36683.

   The stride length is 1.

   <img width="993" alt="bar chart" src="https://github.com/user-attachments/assets/8a862f4e-6327-47a1-b383-65cf2519e776" />
