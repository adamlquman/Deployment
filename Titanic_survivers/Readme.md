<h3>Welcome to Ml Deplyment </h3>
Here I will describe ,how to deploy ML classification model locally using fast_api and joblib to load your model for inferenc prediction
<b>First</b> you have to train your model and save it as <code>model.joblib</code> and you can do with this code
<pre><code>
   X = [[0], [2], [3], [9]]
   y = [0, 2, 5, 4]
  model=RandomForestClassifier      # our model
  model.fit(X,y)
  joblib(model,'R_model.joblib')   # save our model as R_model,joblib</code><pre>
    then creat api with fast api like serever.py file ,this file is very important because local host and model integration can be done in this file .
<b>Then</b> you have to use unicorn to run fast api file in your web server.<br>
    <code>uvicorn server:app --host 0.0.0.0 --port 8000</code>

