
# Concrete compressive strength 

![1_LQg3g36bTRx0ZNytVWm5nA](https://user-images.githubusercontent.com/72031522/148807436-a5badcdc-7c37-4912-a488-de9c0ba0af5c.jpeg)


* The Compressive Strength of Concrete determines the quality of Concrete. This is generally determined by a standard crushing test on a concrete cylinder. This requires engineers to build small concrete cylinders with different combinations of raw materials and test these cylinders for strength variations with a change in each raw material. The recommended wait time for testing the cylinder is 28 days to ensure correct results. This consumes a lot of time and requires a lot of labour to prepare different prototypes and test them. Also, this method is prone to human error and one small mistake can cause the wait time to drastically increase.
* One way of reducing the wait time and reducing the number of combinations to try is to make use of digital simulations, where we can provide information to the computer about what we know and the computer tries different combinations to predict the compressive strength. This way we can reduce the number of combinations we can try physically and reduce the amount of time for experimentation. But, to design such software we have to know the relations between all the raw materials and how one material affects the strength. It is possible to derive mathematical equations and run simulations based on these equations, but we cannot expect the relations to be same in real-world. Also, these tests have been performed for many numbers of times now and we have enough real-world data that can be used for predictive modelling.
* In this project, I analysed Concrete Compressive Strength dataset and build a regression model to predict the concrete compressive strength based on the different features in the training data. 






## Project Architecture:

![architecture](https://user-images.githubusercontent.com/72031522/148809968-ed66c074-991b-4587-8898-4d7c91500621.jpg)



## Data Description :
![datatable1](https://user-images.githubusercontent.com/72031522/148810979-3f7d7698-9aec-4437-a567-25cf2d121aea.png)
![datatable2](https://user-images.githubusercontent.com/72031522/148810993-4b1922e1-386d-48ae-aa77-6a4c93e70ae3.png)


## Demo

Project Folder Structure:

![folderStructure](https://user-images.githubusercontent.com/72031522/148811630-d82f0628-51a1-450b-9c28-507fe76936ba.png)
--------

- main.py is the entry point of our application, where the flask server starts

![main](https://user-images.githubusercontent.com/72031522/148811883-0c8dabb6-2779-403b-b7f2-0f9078512cdb.png)
-------

- This is the predictionFromModel.py file where the predictions take place based on the data we are giving input to the model

![predictionfromModel](https://user-images.githubusercontent.com/72031522/148812113-4f36d212-6f32-4da3-b0bb-55d793eb7be0.png)
-------------

- Now run the main.py file which is entry point of application, The web app link is created by flask,Open the link in browser.

![host_link](https://user-images.githubusercontent.com/72031522/148812322-fbae2ba0-b5ae-418c-a0f9-ab21e19b7e64.png)
-------------

- Open this link in browser, The Home Page of web app will open:

![HomePage](https://user-images.githubusercontent.com/72031522/148813067-7a9b5218-869e-403c-94e3-3af7dfc90e78.png)
-------

- Now enter the folder directory where batch files are stored And click on predict.

![batchfilespredictpath](https://user-images.githubusercontent.com/72031522/148813143-f0da5c12-a9b3-4cc6-abe6-b66600a60e3c.png)
-------

- prediction:

![prediction](https://user-images.githubusercontent.com/72031522/148813262-77073dd1-8171-424f-8418-e567a959ea15.png)

    1) All the files from batch directory are extracted and the data is saved on sql server.
    
    2) Data Export from Db - The data in the stored database is exported as a CSV file to be used for prediction.
    
    3) Clustering - KMeans model created during training is loaded, and clusters for the preprocessed prediction data is predicted.

    4) Prediction - Based on the cluster number, the respective model is loaded and is used to predict the data for that cluster.

    5) Once the prediction is made for all the clusters, the predictions along with the original names before label encoder are saved in a CSV file at a given location and the location is returned to the client.





## Installation

- The Code is written in Python 3.6.10. If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. 
- The all code written through Moduler approach.I suggest to use PyCharm IDE as it is well designed for python.
- Modular programming is a software design technique that emphasizes separating the functionality of a program into independent, interchangeable modules, such that each contains everything necessary to execute only one aspect of the desired functionality.
- Therefore in this project for each funtion different module is made and we just have to import required modules where it is required
- To install the required packages and libraries, run this command in the project directory after cloning the repository.

```bash
pip install -r requirements.txt
```


## Deployement on Heroku

Login or signup in order to create virtual app. You can either connect your github profile or download ctl to manually deploy this project.

[![](https://i.imgur.com/dKmlpqX.png)](https://heroku.com)

Our next step would be to follow the instruction given on [Heroku Documentation](https://devcenter.heroku.com/articles/getting-started-with-python) to deploy a web app.


## Technologies Used

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/flask-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) [<img target="_blank" src="https://number1.co.za/wp-content/uploads/2017/10/gunicorn_logo-300x85.png" width=280>](https://gunicorn.org) [<img target="_blank" src="https://scikit-learn.org/stable/_static/scikit-learn-logo-small.png" width=200>](https://scikit-learn.org/stable/)

[![Heroku](https://github.com/jalbertsr/logo-badge-images/blob/master/img/rsz_heroku.png?raw=true)](https://www.heroku.com/)

[![Python](https://github.com/jalbertsr/logo-badge-images/blob/master/img/rsz_python.png?raw=true)](https://www.python.org/)

<a title="Marc Garcia, BSD &lt;http://opensource.org/licenses/bsd-license.php&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Pandas_logo.svg"><img width="128" alt="Pandas logo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Pandas_logo.svg/128px-Pandas_logo.svg.png"></a>

<a title="JetBrains, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:PyCharm_Icon.svg"><img width="128" alt="PyCharm Icon" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/PyCharm_Icon.svg/128px-PyCharm_Icon.svg.png"></a>
## Bug / Feature Request

If you find a bug (the website couldn't handle the query and / or gave undesired results), kindly open an [issue](https://github.com/Mandal-21/Flight-Price-Prediction/issues) here by including your search query and the expected result


## Deployed Heroku app link

App Link : 