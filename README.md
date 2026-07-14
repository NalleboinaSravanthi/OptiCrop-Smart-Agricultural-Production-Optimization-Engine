# Entity Relationship Diagram (ERD)

## Project

**OptiCrop: Smart Agricultural Production Optimization Engine**

------------------------------------------------------------------------

## Description

The Entity Relationship Diagram (ERD) represents the database structure
of the **OptiCrop** system. It illustrates the entities involved in
storing user information, soil parameters, crop information, datasets,
machine learning models, prediction results, and reports. The ERD helps
organize agricultural data efficiently and supports intelligent crop
recommendation for sustainable farming.

> **Note:** This documentation is based on the ER diagram provided in
> the project resources.

------------------------------------------------------------------------

## ER Diagram

Place the provided ER diagram image in the repository and reference it
as shown below.

``` text
docs/
├── ER_Diagram.md
└── images/
    └── er_diagram.png
```

``` markdown
![Entity Relationship Diagram](images/er_diagram.png)
```

------------------------------------------------------------------------

## Entities Involved

-   User
-   SoilData
-   Crop
-   Dataset
-   MLModel
-   Prediction
-   Report

------------------------------------------------------------------------

## Primary Keys

  Entity       Primary Key
  ------------ ---------------
  User         user_id
  SoilData     soil_id
  Crop         crop_id
  Dataset      dataset_id
  MLModel      model_id
  Prediction   prediction_id
  Report       report_id

------------------------------------------------------------------------

## Foreign Keys

  Entity       Foreign Key     References
  ------------ --------------- ------------
  SoilData     user_id         User
  Prediction   soil_id         SoilData
  Prediction   crop_id         Crop
  Prediction   model_id        MLModel
  Report       prediction_id   Prediction

------------------------------------------------------------------------

## Relationships

-   **User → SoilData:** One-to-Many
-   **SoilData → Prediction:** One-to-One
-   **Crop → Prediction:** One-to-Many
-   **Dataset → MLModel:** One-to-Many
-   **MLModel → Prediction:** One-to-Many
-   **Prediction → Report:** One-to-Many

------------------------------------------------------------------------

## Cardinality

-   One user can submit multiple soil data records.
-   Each soil data record generates one prediction.
-   One crop can be recommended in multiple predictions.
-   One dataset can train multiple machine learning models.
-   One ML model can generate many predictions.
-   One prediction can generate one or more reports.

------------------------------------------------------------------------

## Normalization

The database separates users, soil data, crops, datasets, machine
learning models, predictions, and reports into individual entities. This
reduces redundancy, improves scalability, and maintains data integrity.

------------------------------------------------------------------------

## Use Case Coverage

-   Manage users and soil information.
-   Recommend crops using machine learning.
-   Maintain agricultural datasets and ML models.
-   Store prediction results.
-   Generate agricultural recommendation reports.
-   Support sustainable farming and agricultural research.

------------------------------------------------------------------------

## Conclusion

The ERD provides a structured and scalable database design for the
OptiCrop system, enabling efficient agricultural data management and
accurate crop recommendations.

------------------------------------------------------------------------

## Repository Structure

``` text
docs/
├── ER_Diagram.md
└── images/
    └── er_diagram.png
```
