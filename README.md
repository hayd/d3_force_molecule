<script src="https://raw.github.com/hayd/d3_force_molecule/master/d3_force_molecule.js"></script>
<link rel="stylesheet" href="https://raw.github.com/hayd/d3_force_molecule/master/d3_force_molecule.css" type="text/css"></script>

## d3_force_molecule

We give a javascript function to create a D3 force molecule representation for a provided molecule.
This reuses the work from EvanZ's example: http://www.d3coder.com/2012/07/01/drawing-chemical-structures-with-force-layout/.

For example, to include a diagram for water we first create a div (or span, etc.), say of class "water":

    <div class="water"></div>

Next we describe the molecule of water by listing the elements, and describing the links between them:

    {"molecule":"HHO", "links":[[0, 2], [1, 2]]}

Now call `render_molecule` at the bottom of the page (the last two arguments are the height and width),
selecting the class water in the usual fashion.

    render_molecule(".water", {"molecule":"HHO", "links":[[0, 2], [1, 2]]}, 200, 200);

The actual div just below this line:

<div class="water"></div>

<script type="text/javascript">
  render_molecule(".water", {"molecule":"HHO", "links":[[0, 2], [1, 2]]}, 100, 100);
  render_molecule(".alanine", {"molecule":"CCCNHOOHHHHHH",
                               "links":[[0, 1], [1, 2], [1, 3], [2, 5], [2, 6], [1, 4],
                                      [3, 10], [3, 11], [0, 7], [0, 8], [0, 9], [5, 12]]},
                    200, 200);
</script>