# Calculus Final Exams Table

## Series

**Responsive Web Design — HTML Series #12**

This exercise builds a semantic HTML table for displaying student calculus final exam grades.

## What this exercise teaches

- The `table` element
- `caption` for a table title
- `thead` for table headings
- `tbody` for the main data
- `tfoot` for summary information
- `tr` for table rows
- `th` for header cells
- `td` for data cells
- `colspan` for combining table columns
- Semantic organization of tabular data

---

## Complete code

The complete exercise is stored in `index.html`.

The HTML file contains comments explaining the role of each major table section.

---

## Code walkthrough

### 1. The table element

```html
<table>
  ...
</table>
```

The `table` element creates a table for structured tabular data.

Think:

**table = complete table**

---

### 2. Caption

```html
<caption>
  Calculus Final Exam Grades
</caption>
```

The `caption` describes the purpose or title of the table.

Here, it tells us that the table contains calculus final exam grades.

Memory trick:

**caption = table title**

---

### 3. Table header

```html
<thead>
  <tr>
    <th>Last Name</th>
    <th>First Name</th>
    <th>Grade</th>
  </tr>
</thead>
```

- `thead` contains the table's heading rows.
- `tr` means **table row**.
- `th` means **table header cell**.

The three headings describe the three columns:

1. Last Name
2. First Name
3. Grade

---

### 4. Table body

```html
<tbody>
  <tr>
    <td>Davis</td>
    <td>Alex</td>
    <td>54</td>
  </tr>
</tbody>
```

- `tbody` contains the main data.
- Each `tr` represents one student.
- Each `td` represents one data cell.

Memory trick:

**tbody = main table data**

---

### 5. Table rows

```html
<tr>
  <td>Davis</td>
  <td>Alex</td>
  <td>54</td>
</tr>
```

`tr` creates one horizontal row.

This row contains:

- Last name → Davis
- First name → Alex
- Grade → 54

So:

**tr = table row**

---

### 6. Table data cells

```html
<td>Davis</td>
<td>Alex</td>
<td>54</td>
```

`td` means **table data**.

Every `td` contains one piece of data in the table.

Memory trick:

**td = table data**

---

### 7. Table footer

```html
<tfoot>
  <tr>
    <td colspan="2">Average Grade</td>
    <td>78.8</td>
  </tr>
</tfoot>
```

The `tfoot` contains summary information for the table.

Here it displays the average grade.

---

### 8. Understanding colspan

The important part is:

```html
<td colspan="2">Average Grade</td>
```

Normally, one `td` occupies one column.

With:

```
colspan="2"
```

the cell occupies **two columns**.

The footer therefore looks conceptually like:

```
┌────────────────────────┬─────────┐
│      Average Grade     │  78.8   │
│       2 columns        │ 1 col.  │
└────────────────────────┴─────────┘
```

Memory trick:

**colspan = span across columns**

---

## Table structure to remember

```text
<table>
│
├── <caption> → table title
│
├── <thead> → headings
│   └── <tr> → row
│       └── <th> → header cells
│
├── <tbody> → main data
│   └── <tr> → rows
│       └── <td> → data cells
│
└── <tfoot> → summary/footer
    └── <tr> → row
        └── <td> → summary cells
```

---

## Important difference: th vs td

| Element | Meaning | Purpose |
|---|---|---|
| `th` | Table Header | Heading/label |
| `td` | Table Data | Actual data |

Example:

```html
<th>Grade</th>
<td>92</td>
```

**Grade** is the heading, while **92** is the data.

---

## Quick revision

### Table

`<table>` → creates the table.

### Caption

`<caption>` → describes/titles the table.

### Header

`<thead>` → contains heading rows.

### Header cell

`<th>` → heading cell.

### Body

`<tbody>` → contains the main data.

### Data cell

`<td>` → normal data cell.

### Row

`<tr>` → table row.

### Footer

`<tfoot>` → summary/footer information.

### Column spanning

`colspan="2"` → one cell covers two columns.

---

## Common mistakes

### 1. Confusing th and td

Wrong idea:

`<td>` is for headings.

Correct:

`<th>` is for headings and `<td>` is for normal table data.

### 2. Confusing colspan with rowspan

- `colspan` → spans across **columns**
- `rowspan` → spans across **rows**

### 3. Forgetting that tr means row

`tr` = **table row**

### 4. Forgetting semantic table sections

For a structured table, remember:

```text
caption → title
thead   → headings
tbody   → main data
tfoot   → summary
```

---

## Final revision map

```text
TABLE
│
├── caption → title
│
├── thead
│   └── tr
│       └── th
│
├── tbody
│   └── tr
│       └── td
│
└── tfoot
    └── tr
        └── td + colspan
```

## One-line takeaway

**A semantic HTML table uses caption, thead, tbody, tfoot, tr, th, and td to organize tabular information clearly.**

## Files

- `index.html` — complete commented Calculus Final Exams table
- `README.md` — detailed explanation and revision notes
