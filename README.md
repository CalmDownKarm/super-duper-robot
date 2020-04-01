# quickdirty

## Setup

- [Install Gramex 1.x](https://learn.gramener.com/guide/install/)
- Clone this repository
- Copy assets from shared repo, e.g. `demo.gramener.com:/deploy/<user>/<repo>/`
- From the repo folder, run `gramex setup .`
- From the repo folder, run `gramex`

## data set up
- Your data files should ideally be in assets/data/
- Each File should have a minimum of 3 columns, an id column, Tweet column and Class column.
- Class column should be 0 for all rows.
- set data file name in gramex.yaml - for example
```
quickdirty-formhandler:
    pattern: /$YAMLURL/data
    handler: FormHandler
    kwargs:
      url: $YAMLPATH/assets/data/<data-file-name>
      id: id
      default:
        Class: 0
```
Put labels in labels.csv (also in assets/data)
## Contributions

- calmdownkarm <karmanyaaggarwal@gmail.com>
