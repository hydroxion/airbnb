# Airbnb

Airbnb rent price forecasting.

## Setup

Use the package manager APT to install the general dependencies.

```sh
apt install python3 python3-dev python3-pip python3-venv
```

Use the Python 3 to create a virtual environment.

```sh
python3 -m venv venv
```

Activate the virtual environment.

```sh
source ./venv/bin/activate
```

Use the package manager Pip to install the dependencies.

```sh
pip3 install -r requirements.txt
```

Use the Jupyter package to enable the extensions.

```sh
jupyter nbextension enable --py widgetsnbextension
```

## Usage

Start a Jupyter Lab server.

```sh
jupyter lab --log-level=critical
```

Open the _main.ipynb_ notebook and execute all cells.

## Documentation

The dataset [source](http://insideairbnb.com/get-the-data.html) (Rio de Janeiro).

## Q&A

- How was the modeling strategy defined?

Bootstrap and boosting tree models are fit to the task in terms of feature coverage, optimization and explainability.

- How was the cost function used defined?

Regression models are normally evaluated by the mean squared error (MSE), a.k.a the distance between truthy and predicted values.

- What was the criterion used to validate the model?

Bootstrap and boosting tree models improve stability and accuracy, making root mean squared error (RMSE) a better and balanced fit to evaluate the model performance in the context of large errors, i.e in the context of features like price that by nature has a high deviation that can lead to high error.

- What evidence is there to define the model as good?

Both the tree bias and the RMSE are in a low scale of 0.00\* and the feature importance visualization doesn't indicate overfiting or underfiting, besides the fact that random search optimization is used to define the hyperparameters.

## Contributing

Pull requests are welcome. Please, consider the following.

1. Make sure your code is standardized
2. Make sure your code is secure
3. Make sure your code is fast
4. Make sure your code is documented
5. Describe the changes that were done

> No issue or PR template required, but be informative

## License

[MIT](./LICENSE.md)
