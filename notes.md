# Notes of the class

## tidyverse package

- ``|>`` introuces the object as first argument of the function.
    - ``penguins |> head()`` to see the headline of dataset penguins.
    - Useful together with ``filter`` and ``group_by`` for descriptive statistics:
        - ``penguins |> filter(!is.na(sex)) |> group_by(sex) |> summarize()``

- ``penguins |> janitor::tabyl()`` for decriptive tables. Better than table(), because it allows the output table to be saved.
- ``left_join()`` faster alternative to ``merge()``.
    - ``suffix`` argument allows us to change names of the variable that is emplyed for the merging.
- ``pivot_longer()``, ``pivot_wider()`` the new version of ``cast()``, ``dcast()`` ``melt()``.

## ggplot2 basics

- ggplot meaning grammar of graphics.
- Connects layers by ``+`` instead of ``|>``.
    - still, ``penguins  |> ggpot(aes(x = , y = )) + geom_point()``
- ``facet_wrap()`` generates several graphs by category, with shared axes.
