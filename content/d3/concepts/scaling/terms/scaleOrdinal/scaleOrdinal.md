---
Title: 'D3.scaleOrdinal()' 

Subjects: 
  - 'Data Visualization'
  - 'Data Science'
  - 'Web Development'
  
Tags:
  - 'D3'
  - 'Data'
  - 'Charts'
  
CatalogContent:
  - 'learn-d3'
  - 'paths/data-science'
---

The **D3.scaleOrdinal()** function is used to build an ordinal scale which has identified range with input values and domain with output values. If none of these values are given for the domain or range, then both are moved to an empty array. 

Ordinal scales are mostly used for names and categorical data where there is a distinct set of values (e.g: categories, colors, or labels), however, the output values can be anything including strings or numbers. The scale portrays a set of discrete input values which is the **domain** to compatible batch of output values which is called the **range**. Please note that the order of the data matters.

## Syntax

D3.scaleOrdinal() generally takes the following form:

```pseudo
d3.scaleOrdinal([[domain, ]range]);               //Creating an ordinal scale
```

**domain**
    This domain is the input value that will be mapped. it defines the minimum and maximum values for the scale.
    
**range**
    The range is the output value that will be mapped. Every value in domain synchronize with value in the range.
    
**return value**
This function does not return anything.
    
## Example
The code snippet is paricularly useful in data visualization tasks where you need consistently need to map specific categories (like numbers to positions).


```codebyte/jscode
const positionScale = d3.scaleOrdinal()
                    .domain(['First', 'Second', 'Third'])
                    .range([5.33, 5.45, 6.03]);

// Example usage:
console.log(positionScale('First'));  // Output: '5.33'
console.log(positionScale('Second')); // Output: '5.45'
console.log(positionScale('Third')); // Output: '6.03'
```

Three runners are competiting in a race. The first person finishes the race in five minutes and thirty-three seconds while the second person finishes the race in five minutes and forty-five seconds. The third person finishes the race in six minutes and three seconds. From the data visualization tasks, we can deduct the different positions and differences from the value of the range. Without the range, it would be impossible to get more data about the domain.