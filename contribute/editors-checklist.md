---
title: Editors checklist
summary: Checklist for editors before approving and merging a pull request (PR).
---

## Before approving and merging a pull request (PR), the editors must check that
1. The page layout in preview looks correct.
2. The new page is linked in the appropriate [sidebar](https://github.com/elixir-europe/infectious-diseases-toolkit/tree/main/_data/sidebars) menu, in the same branch of the PR.
3. The contributors' names are listed in the [CONTRIBUTORS file](https://github.com/elixir-europe/infectious-diseases-toolkit/blob/main/_data/CONTRIBUTORS.yaml), in the same branch of the PR. Advice to have at least one  contributor per page having its contact information in this  [CONTRIBUTORS file](https://github.com/elixir-europe/infectious-diseases-toolkit/blob/main/_data/CONTRIBUTORS.yaml).
4. All relevant metadata fields in a specific page are correctly filled in (see the [page metadata](/contribute/page-metadata) and the [Editorial board guide](/contribute/editorial-board-guide)). Some critical ones are listed below.
   * unique `page_id` ([List of page IDs](/contribute/website-overview))
   * `contributors`
   * `related_pages` ([Related pages](/contribute/editorial-board-guide.html#related-pages))
   * `training`
   * `search_exclude` must be deleted
   * `description`
   * `affiliation`
   * `coordinators`(only used in national pages + they must be listed as `contributors` as well)
   * `resources`
5. Items in the "[Tools and resources spreadsheet](https://docs.google.com/spreadsheets/d/13tqfSbgivokfEkxGXPRFShVhCmO4VuTQRe4uQgJOMbc)" are tagged with already existing (merged) `page_id` from "Pathogen characterisation, Socioeconomic data, Human biomolecular data, Human clinical and health data, Showcase" and that Bert has been informed of the changes.
6. The content is within the scope of the Infectious Diseases Toolkit (prevent overlap with the [RDMkit](https://rdmkit.elixir-europe.org/) and link towards it instead), conforms to the appropriate templates and the [style](/contribute/style-guide).
7. There are no [copyright](/contribute/copyright) issues related to the content of the page.
8. The contributors implemented the requested changes.
9.  When a new page is added, a news item is added to the [news.yml file](https://github.com/elixir-europe/infectious-diseases-toolkit/blob/main/_data/news.yml), in the same branch of the PR.
10. The contributors are thanked for their effort and informed about the publication of their content.
11. The PR is linked to related issues and can be merged in main branch with no conflicts.
