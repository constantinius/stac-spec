# STAC Datasets

[Items](https://github.com/radiantearth/stac-spec/item-spec/) are focused on search within a dataset*. Another topic of interest is the search of datasets, instead of within a dataset. The Dataset Spec is independent of Items and [Catalogs](../catalog-spec/). STAC Items are *strongly recommended* to provide a link to a dataset definition. Other parties can also independently use this spec to describe datasets in a lightweight way. Datasets are defined in full in the 
Dataset Specification.

The Datasets Spec extends the [Catalog Spec](../catalog-spec/) with additional fields to describe the set of items in the catalog. It shares the same fields and therefore every Dataset is also a valid Catalog. Datasets can have both parent Catalogs and Datasets and child Items, Catalogs and Datasets. 

*\* There is no standardized name for the concept we are describing here. Others called it: dataset series (ISO 19115), collection (CNES, NASA), dataset (JAXA), dataset series (ESA), product (JAXA).*

## In this directory

**The Specification:** The main Dataset specification is in *[dataset-spec.md](dataset-spec.md)*. It includes an overview and in depth explanation of the 
structures and fields.

**Examples:** For samples of how Datasets can be implemented the *[examples/](examples/)* folder contains a sample dataset. 

**Schemas:** The schemas to validate the core `Dataset` definition are found in the 
*[json-schema/](json-schema/)* folder. The primary one is *[dataset.json](json-schema/dataset.json)*.


## Schema Validation

Instruction on schema validation for STAC Items can be found in the [validation instructions](validation/README.md).

## Dataset Flexibility

STAC Datasets are defined for flexibility. They only require a handful of fields, and
implementors are free to add most any JSON field or object that they want via extensions. This is a design goal, so
that it is quite easy to implement a dataset and be able to adapt it to most any data model.

But it is expected that some more firm recommendations and even requirements will emerge, so that clients will be able to glean
more meaningful information. In the meantime implementors are encouraged to do what makes sense for
them, and to check out the [examples](examples/) and [other implementations](../implementations.md) for emerging best practices.

## Dataset Evolution 

The Dataset specification is maturing, but it is still relatively early days. As real world
implementations innovate in different ways, we will update the core fields to handle.