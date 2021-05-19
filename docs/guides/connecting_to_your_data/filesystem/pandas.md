---
title: How to connect to your data on a filesystem using pandas
---
import NextSteps from '../components/next_steps.md'
import Congratulations from '../components/congratulations.md'
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

This guide will help you connect to your data stored on a filesystem using pandas.
This will allow you to validate and explore your data.

:::note Prerequisites: This how-to guide assumes you have already:
- Completed the [Getting Started Tutorial](../../../tutorials/getting-started/intro.md)
- Have a working installation of Great Expectations
- Have access to data on a filesystem
:::

## Steps

### 1. `[🍏 CORE SKILL ICON]` Instantiate your project's DataContext

Create a Jupyter notebook or script in the same directory as the `great_expectations/` directory.
Import these necessary packages and modules.

```python file=../../../../integration/code/connecting_to_your_data/filesystem/pandas_example.py#L1-L3
```

Load your DataContext into memory using the `get_context()` method.

```python file=../../../../integration/code/connecting_to_your_data/filesystem/pandas_example.py#L6
```

### 2. Write your YAML Datasource configuration

Using this example configuration:

```python file=../../../../integration/code/connecting_to_your_data/filesystem/pandas_example.py#L8-L20
```

### 3. Save the Datasource configuration to your DataContext

Save the configuration into your `DataContext` by using the `add_datasource()` function.

```python file=../../../../integration/code/connecting_to_your_data/filesystem/pandas_example.py#L22
```

### 4. Test your new Datasource

Verify your new Datasource by loading data from it into a `Validator` using a `BatchRequest`.

Add the path to your CSV in the `path` key under `runtime_parameters`.

```python file=../../../../integration/code/connecting_to_your_data/filesystem/pandas_example.py#L24-L44
```

<Congratulations />

## Additional Notes

To view the full script [see it on GitHub](https://github.com/great-expectations/great_expectations/blob/knoxpod/integration/code/connecting_to_your_data/filesystem/pandas_example.py)

If you are working with nonstandard CSVs, read one of these guides:

- [How to work with headerless CSVs in pandas](#TODO)
- [How to work with custom delimited CSVs in pandas](#TODO)
- [How to work with parquet files in pandas](#TODO)

## Next Steps

<NextSteps />