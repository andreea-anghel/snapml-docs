Model Import
============

Snap ML supports importing tree ensembles models that were trained with other frameworks (e.g., scikit-learn, XGBoost, LightGBM) so one can leverage Snap ML's accelerated inference engine.
One can import a model either by:

* instantiating the corresponding Snap ML class (e.g., :class:`snapml.RandomForestClassifier`) and then call the :func:`import_model` member function (e.g., :func:`snapml.RandomForestClassifier.import_model`)
* calling the generic :func:`snapml.import_model` function documented below, which will detect the type of model from the model file and return the corresponding Snap ML class.

Details regarding which Snap ML classes can import which types of pre-trained model, and which model formats are supported are given in the following table:

+--------------------------------------------------+-------------------+-------------------------------------------+
| Pre-trained Model                                | Supported Formats | Target Snap ML Class                      |
+==================================================+===================+===========================================+
| :class:`xgboost.XGBClassifier`                   | PMML, ONNX, JSON  | :class:`snapml.BoostingMachineClassifier` |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`xgboost.XGBRegressor`                    | PMML, ONNX, JSON  | :class:`snapml.BoostingMachineRegressor`  |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`lightgbm.LGBMClassifier`                 | PMML, ONNX, Text  | :class:`snapml.BoostingMachineClassifier` |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`lightgbm.LGBMRegressor`                  | PMML, ONNX, Text  | :class:`snapml.BoostingMachineRegressor`  |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`snapml.BoostingMachineClassifier`        | PMML              | :class:`snapml.BoostingMachineClassifier` |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`snapml.BoostingMachineRegressor`         | PMML              | :class:`snapml.BoostingMachineRegressor`  |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`sklearn.ensemble.RandomForestClassifier` | PMML, ONNX        | :class:`snapml.RandomForestClassifier`    |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`sklearn.ensemble.RandomForestRegressor`  | PMML, ONNX        | :class:`snapml.RandomForestRegressor`     |
+--------------------------------------------------+-------------------+--------+----------------------------------+
| :class:`sklearn.ensemble.ExtraTreesClassifier`   | PMML, ONNX        | :class:`snapml.RandomForestClassifier`    |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`sklearn.ensemble.ExtraTreesRegressor`    | PMML, ONNX        | :class:`snapml.RandomForestRegressor`     |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`snapml.RandomForestClassifier`           | PMML              | :class:`snapml.RandomForestClassifier`    |
+--------------------------------------------------+-------------------+-------------------------------------------+
| :class:`snapml.RandomForestRegressor`            | PMML              | :class:`snapml.RandomForestRegressor`     |
+--------------------------------------------------+-------------------+-------------------------------------------+

.. autofunction:: snapml.import_model
