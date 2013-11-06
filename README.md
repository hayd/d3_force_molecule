## d3_force_molecule

We give a javascript function to create a D3 force molecule representation for a provided molecule.
,
For example:

HOH -> gives the D3 repr for H20

Note: should this work for H20.

Similarly for larger molecules.

This works in two parts:

First, given a repr for a molecule it defines an array of molecules and a list of links between these. Second, given this list it creates the D3 objects. This essentially follows the EvanZ's example: http://www.d3coder.com/2012/07/01/drawing-chemical-structures-with-force-layout/.
