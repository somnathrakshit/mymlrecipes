---
html_meta:
  "description lang=en": "Interview resource of Data Science Interview focusing on Excel basics."
  "keywords": "interview, Excel, practice questions"
  "property=og:locale": "en_US"
---

## Excel Basics

```{warning}
This page is a work in progress
```

```{figure} images/image1.png
---
name: image1
scale: 50%
---
```

---

### Questions

```{admonition} Problem: Find the Revenue
:class: tip, dropdown

From the source below can you find the Revenue the specified account?

![Table](images/image2.png)

```

```{admonition} Solution:
:class: dropdown
This can be solved with a simple VLOOKUP, the formula to find the answer is given below:

`
	=VLOOKUP(F3,B2:D12,3,FALSE)
`

```

```{admonition} Problem: Find the Customer Number
:class: tip, dropdown

From the source below can you find the Customer Number corresponding to the Account Name?

![Table](images/image3.png)

```

```{admonition} Solution:
:class: dropdown
VLOOKUP won't work as Customer Num is to the LEFT of the Account Name. We need INDEX MATCH [📖Explanation](https://exceljet.net/index-and-match)

`
	=INDEX(A2:D12,MATCH(F7,B2:B12),1)
`

```

```{admonition} Problem: Total Revenue per Sales Rep
:class: tip, dropdown

From the source below can you find the total revenue per sales rep?

![Table](images/image4.png)

```

```{admonition} Solution:
:class: dropdown
This can be solved with a simple SUMIF. For the first row the answer is given below. It will be similar for other rows.
`
	=SUMIF(C3:C12,"="&F11,D3:D12)
`

```