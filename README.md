# marcell66

#imperative

result = []
i = 0
start:
numPeople = length(people)
if i >= numPeople goto finished
p = people[i]
nameLength = length(p.name)
if nameLength <= 5 goto nextOne
upperName = toUpper(p.name)
addToList(result, upperName)
nextOne:
i = i + 1
goto start
finished:
return sort(result)
    
#structured

result = [];
for i = 0; i < length(people); i++ {
p = people[i];
if length(p.name)) > 5 
addToList(result, toUpper(p.name));
} }
return sort(result);

#oop

result := List new.
people each: [:p |
p name length greaterThan: 5 ifTrue: [result add (p name upper)]
]
result sort.
^result

#This can be shortened to: 
^people filter: [:p | p name length greaterThan: 5] map: [:p | p name upper] sort

result = []
for p in people {
if p.name.length > 5 {
result.add(p.name.toUpper);
}
}
return result.sort;

#Declarative Programming

select upper(name)
from people
where length(name) > 5
order by name

