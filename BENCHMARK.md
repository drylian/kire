# Kire Performance Benchmarks

This report compares **Kire** directives, elements, and components with other popular template engines in various scenarios. Benchmarks are executed in isolated worker processes to ensure fair comparisons. Templates are precompiled once per engine before the timed loop.

Generated on: Wed, 19 Aug 2026 19:15:44 GMT

## Runtime: BUN

### Scenario: Small Data (10 items, 10000 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| kire | 814,538 | **Fastest** | `####################` |
| kire_elements | 813,675 | 99.9% | `####################` |
| pug | 688,922 | 84.6% | `#################---` |
| kire_components | 602,003 | 73.9% | `###############-----` |
| nunjucks | 281,019 | 34.5% | `#######-------------` |
| edge.js | 264,294 | 32.4% | `######--------------` |
| handlebars | 234,536 | 28.8% | `######--------------` |
| ejs | 60,020 | 7.4% | `#-------------------` |

### Scenario: Medium Data (100 items, 1000 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| kire_elements | 101,159 | **Fastest** | `####################` |
| kire | 99,932 | 98.8% | `####################` |
| pug | 80,251 | 79.3% | `################----` |
| kire_components | 75,283 | 74.4% | `###############-----` |
| edge.js | 38,522 | 38.1% | `########------------` |
| nunjucks | 31,595 | 31.2% | `######--------------` |
| handlebars | 27,922 | 27.6% | `######--------------` |
| ejs | 6,393 | 6.3% | `#-------------------` |

### Scenario: Large Data (1000 items, 100 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| kire | 11,354 | **Fastest** | `####################` |
| kire_elements | 10,858 | 95.6% | `###################-` |
| pug | 8,844 | 77.9% | `################----` |
| kire_components | 7,605 | 67.0% | `#############-------` |
| edge.js | 4,404 | 38.8% | `########------------` |
| nunjucks | 3,406 | 30.0% | `######--------------` |
| handlebars | 2,904 | 25.6% | `#####---------------` |
| ejs | 650 | 5.7% | `#-------------------` |

## Runtime: DENO

### Scenario: Small Data (10 items, 10000 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| pug | 699,459 | **Fastest** | `####################` |
| kire | 497,400 | 71.1% | `##############------` |
| kire_elements | 495,374 | 70.8% | `##############------` |
| kire_components | 417,814 | 59.7% | `############--------` |
| edge.js | 216,875 | 31.0% | `######--------------` |
| handlebars | 196,883 | 28.1% | `######--------------` |
| nunjucks | 113,120 | 16.2% | `###-----------------` |
| ejs | 99,987 | 14.3% | `###-----------------` |

### Scenario: Medium Data (100 items, 1000 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| pug | 76,411 | **Fastest** | `####################` |
| kire_elements | 53,499 | 70.0% | `##############------` |
| kire | 52,989 | 69.3% | `##############------` |
| kire_components | 46,865 | 61.3% | `############--------` |
| edge.js | 26,491 | 34.7% | `#######-------------` |
| handlebars | 23,478 | 30.7% | `######--------------` |
| nunjucks | 12,000 | 15.7% | `###-----------------` |
| ejs | 10,616 | 13.9% | `###-----------------` |

### Scenario: Large Data (1000 items, 100 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| pug | 7,916 | **Fastest** | `####################` |
| kire_elements | 5,388 | 68.1% | `##############------` |
| kire | 5,275 | 66.6% | `#############-------` |
| kire_components | 4,526 | 57.2% | `###########---------` |
| edge.js | 2,790 | 35.2% | `#######-------------` |
| handlebars | 2,453 | 31.0% | `######--------------` |
| nunjucks | 1,186 | 15.0% | `###-----------------` |
| ejs | 1,065 | 13.5% | `###-----------------` |

## Runtime: NODE

### Scenario: Small Data (10 items, 10000 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| kire_elements | 758,258 | **Fastest** | `####################` |
| pug | 749,576 | 98.9% | `####################` |
| kire | 738,364 | 97.4% | `###################-` |
| kire_components | 648,695 | 85.6% | `#################---` |
| edge.js | 229,113 | 30.2% | `######--------------` |
| handlebars | 200,394 | 26.4% | `#####---------------` |
| nunjucks | 127,425 | 16.8% | `###-----------------` |
| ejs | 100,588 | 13.3% | `###-----------------` |

### Scenario: Medium Data (100 items, 1000 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| kire | 93,496 | **Fastest** | `####################` |
| kire_elements | 92,461 | 98.9% | `####################` |
| pug | 82,655 | 88.4% | `##################--` |
| kire_components | 78,092 | 83.5% | `#################---` |
| edge.js | 29,352 | 31.4% | `######--------------` |
| handlebars | 25,087 | 26.8% | `#####---------------` |
| nunjucks | 14,214 | 15.2% | `###-----------------` |
| ejs | 10,964 | 11.7% | `##------------------` |

### Scenario: Large Data (1000 items, 100 iterations)

| Engine | Ops/sec | Speed | Visual |
| :--- | :--- | :--- | :--- |
| kire_elements | 9,073 | **Fastest** | `####################` |
| kire | 8,942 | 98.6% | `####################` |
| pug | 8,271 | 91.2% | `##################--` |
| kire_components | 7,682 | 84.7% | `#################---` |
| edge.js | 2,961 | 32.6% | `#######-------------` |
| handlebars | 2,469 | 27.2% | `#####---------------` |
| nunjucks | 1,411 | 15.6% | `###-----------------` |
| ejs | 1,293 | 14.3% | `###-----------------` |

---
*Note: Benchmarks performed using automated GitHub Actions in isolated workers. Performance may vary between environments.*
