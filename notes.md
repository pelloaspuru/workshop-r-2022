# My notes of the class

This are a bunch of notes taken by Pello Aspuru about the R class by Kazuharu.

- Check R version by running ``R.Version()``.

## tidyverse package

- ``|>`` introuces the object as first argument of the function.
    - ``penguins |> head()`` to see the headline of dataset penguins.
    - Useful together with ``filter`` and ``group_by`` for descriptive statistics:
        - ``penguins |> filter(!is.na(sex)) |> group_by(sex) |> summarize()``

- ``penguins |> janitor::tabyl()`` for decriptive tables. Better than table(), because it allows the output table to be saved.
- ``left_join()`` faster alternative to ``merge()``.
    - ``suffix`` argument allows us to change names of the variable that is emplyed for the merging.
- ``pivot_longer()``, ``pivot_wider()`` the new version of ``cast()``, ``dcast()`` ``melt()``.
- ``glimpse()`` to get a glimpse of the data.

## ggplot2 basics

- ggplot meaning grammar of graphics.
- Connects layers by ``+`` instead of ``|>``.
    - still, ``penguins  |> ggpot(aes(x = , y = )) + geom_point()``
- ``facet_wrap()`` generates several graphs by category, with shared axes.
- ``coord_cartesian()`` to zoom in an area, while keeping the observations outside the range to compute fit line, for instance.

## ggplot2 advanced

- changing fonts: ``font_add_google()`` and ``showtext_auto()``.
- Set up plot theme globally ``theme_set()`` and ``theme_update``.
- Third-party themes: ``hrbrthemes``, ``ggpubr``
- save different graphs all as one: ``patchwork`` package.
- save graphs as ``.pdf`` vector format (scalable). 

## Tables

- Descriptive tables: ``kableExtra`` package. to generate latex tables.
- Regression tables: ``fixest`` package and ``modelsummary()`` function for regression table.

## Writing clean code

- Variable naming
    - For TRUE/FALSE variables: ``female`` -> ``is_female``. ``no_kids`` -> ``has_kids``.
    - For binned variables: ``age_bin5``.
- lubridate package. Date and time handling.
- ``recode_factor()``. Takeas a factor variable and renames the different categories within it.
- Parquet format to save datasets.
    - For large datasets, you can first filter the parquet dataset and then load the subset you are interested in as a dataframe.
- GGplot

## Quarto

- Quarto markdown .``qmd``.
- Good format to present code, as allows to combine code and text.

