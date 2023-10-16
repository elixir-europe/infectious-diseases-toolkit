---
title: Add new tool or resource
summary: How to add a tool or resource to Infectious diseases toolkit
search_exclude: true
---

## Way of working

The tools or resources you find on pages are a set selected from a [bigger list](all_tools_and_resources). This selection is based on the appearance of the tool or resource in the content of the page.

The [all_tools_and_resources](all_tools_and_resources) list is based on the [yaml file](https://github.com/bedroesb/infectious-diseases-toolkit/blob/new-way-tag-tools/_data/tool_and_resource_list.yml) in the `_data` directory of the  Infectious Diseases Toolkit repository. Tools and resources can be manually linked to their entry in [FAIRsharing.org](https://fairsharing.org/), [Bio.tools](https://bio.tools) and [TeSS](https://tess.elixir-europe.org/). In addition, every week we run an automatic check to identify entries of the tools and resources in these registries and add the appropriate link to the list. A GitHub Bot will generate a Pull Request (PR) with the new links added to the main data file of the website.

{% include callout.html type="important" content="The link with FAIRsharing,TeSS and Bio.tools is automatically done using GitHub actions and is weekly updated. If no FAIRsharing ID, Bio.tools ID or TeSS Query is available for a source, but there is yet one automatically given (faulty), you can overwrite the automatic linking by adding 'NA' as registry." %}

## The main yaml file

Each tool or resource mentioned in the text has metadata stored in the [main yaml file](https://github.com/elixir-europe/infectious-diseases-toolkit/blob/main/_data/tool_and_resource_list.yml). The metadata block for each tool consists of 5 attributes:
- **id**: The ID of a tool, in kebab-case, lowercase with hyphens.
- **name**: The name of the tool or resource.
- **url**: URL to the main page of the tool or resource. Make sure to start the URL with `https://`.
- **description**: A short description of the tool or resource. Try to not use the characters `"` or `'` .
- **registry**: 3 registries are supported: [Bio.tools](https://bio.tools), [FAIRsharing.org](https://fairsharing.org/) and [TeSS](https://tess.elixir-europe.org/). The keywords you can use respectively are: `biotools`, `fairsharing`, `fairsharing-coll` and `tess`, specifying the id or query with a colon. FAIRsharing collections have an ID that follows the pattern `bsg-s000XXX`. List registries under the `registry` attribute as `key: value pairs`. If no FAIRsharing ID, Bio.tools ID or TeSS Query is available for a source, you can overwrite the automatic linking by adding 'NA' as registry.

Example:

```yml
- id: github
  name: GitHub
  url: https://github.com
  description:
    Versioning system, used for sharing code, as well as for sharing of
    small data
  registry:
    tess: GitHub
```


## What tool or resource can be added to the table
Tools and resources specifically mentioned in the text of the pages should be present in the main table. 

## Making changes

1. Make sure the tool you want to add is not yet already described in the [yaml file](https://github.com/bedroesb/infectious-diseases-toolkit/blob/new-way-tag-tools/_data/tool_and_resource_list.yml). If so, go to step 3, if not, follow the next step.

1. Click on the pencil icon seen on GitHub of the [main yaml file](https://github.com/elixir-europe/infectious-diseases-toolkit/blob/main/_data/tool_and_resource_list.yml) as described in our [GitHub Guide](/contribute/github-way). Add your tool or resource at the bottom of the file following the structure described in the [The main yaml file section of this page](#the-main-yaml-file). Make sure the indentation follows the one of the previous listed items. Copy the content of the yaml file and paste it in an online yaml validator in case of doubt.

1. Copy the `tool_id` of the tool or resource.

1. Add the right context on Infectious Diseases Toolkit for the tool by mentioning it somewhere in the text using the following syntax:
  
  ```
  {% raw %}
  {% tool "tool_id" %}
  {% endraw %}
  ```

  {% include callout.html type="important" content="Don't forget to add the `\"` double quotes around the tool_id and make sure to use the exact tool_id as described in the yaml file." %}

  Example:

  ```
  {% raw %}
  {% tool "github" %} is a powerful data publication service, which is supported by the European commission and focused on research data, including supplemental material like software, tables, figures or slides.
  {% endraw %}
  ```
  Will give: 
  
  {% tool "github" %} is a powerful data publication service, which is supported by the European commission and focused on research data, including supplemental material like software, tables, figures or slides.
