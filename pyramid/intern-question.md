# Intern Question 

## Context: 
There are subtle assumptions baked into the American framing of education that have enormous impact on the structure of education.

*Assumption*: Students _require_ a Teacher with Expertise (i.e. credentials) to teach. 

*Consequence*: A scarcity of teachers relative to students means students must be batched per teacher -- there must be classes. Classes must be taught at one speed, slowing down precocious students and rushing struggling students.   

*Alternative Assumption*: Rather than a Credentialed Teacher, what if experienced students could teach instead? 

*Consequence*: Student-teacher parity means classes are _unnecessary_ and students can _learn at their own pace_.

## Expressing the Situation

Teaching _lineage_* of Amy: 
```
        [ Amy ]
        /     \
    [ Bob ]   [ Fil ]
    /     \         \
[ Dan ]   [ Ann ]   [ Lua ]
      \             /     \
      [ Will ][ May ]     [ Cindy ]
```

*In the Guru-Shishya tradition, "parampara" refers to the succession of knowledge from one generation to the next and translates to "lineage" 

```
// Golang 
type Student struct {
    Name string 
    Teacher  *Student
    Pupils []*Student 
}
```

## Problem 1: Finding Lineages 
Given the root of the tree (Amy), how would you make a function to calculate the lineage of a name?  

Any way to prevent redundant calculation? 

## Problem 2: How to incentivize students to teach? 

Pyramid Schemes!  

Picture that each of students get payment upfront and/or get a fraction of _their_ students' teaching income. 

```
// Golang 
type Student struct {
    Name string 
    Teacher  *Student
    Pupils []*Student

    Cost int // e.g. 100 
    Garnishment int // Percentage expressed as a fraction, e.g. 0.1  
}
```

Given the root of the tree (Amy), where the tree denotes a teaching arrangement in a single period, how could you calculate each teacher's income? 