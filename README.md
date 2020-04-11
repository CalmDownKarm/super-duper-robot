# quickdirty

## Setup

- [Install Gramex 1.x](https://learn.gramener.com/guide/install/)
- Clone this repository
- Copy assets from shared repo, e.g. `demo.gramener.com:/deploy/<user>/<repo>/`
- From the repo folder, run `gramex setup .`
- From the repo folder, run `gramex`

## data set up
- Your data files should ideally be in assets/data/
- Each File should have a minimum of 3 columns, an id column, Text column and Class column.
- Class column should be No Label for all rows that you want to label.
- set data file name in gramex.yaml - for example
```
quickdirty-formhandler:
    pattern: /$YAMLURL/data
    handler: FormHandler
    kwargs:
      url: $YAMLPATH/assets/data/<data-file-name>
      id: id
```
Put labels in labels.csv (also in assets/data)
## Editing Mistaken Annotations
/edit endpoint exposes a table where you can edit the annotations

## Things it does not do
- Handle multiple users. You need to run an instance for each user
- auto create the Class and id columns
- random shuffle the data
- any of the fancy active learning things that Prodigy.ai does




## Contributions

- calmdownkarm <karmanyaaggarwal@gmail.com>
