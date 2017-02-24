# Convert flat list to hierarchy

This is a demo function which takes a flat list having the parent and child and converts the same in hierarchy.

In C# LINQ, you may like to create an extension menthod like [this](http://www.aspnetajaxtutorials.com/2015/03/how-to-convert-flat-list-to.html).

## Input

```` js
[
  {
    id: 1,
    title: 'home',
    parent: null
  },
  {
    id: 2,
    title: 'about',
    parent: null
  },
  {
    id: 3,
    title: 'team',
    parent: 2
  },
  {
    id: 4,
    title: 'company',
    parent: 2
  }
]

## Output

```` js

[
	{
		"id": 1,
		"title": "home",
		"parent": null,
		"children": []
	},
	{
		"id": 2,
		"title": "about",
		"parent": null,
		"children": [
			{
				"id": 3,
				"title": "team",
				"parent": 2,
				"children": []
			},
			{
				"id": 4,
				"title": "company",
				"parent": 2,
				"children": []
			}
		]
	}
]

````