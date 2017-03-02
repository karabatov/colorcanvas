# ColorCanvas

A tool for visualizing and improving the coverage of a mostly HSB color space
with named colors.

An image of the tool in action. When provided a list of colors and matching
names, for each point (color) in the given color space ColorCanvas determines
the nearest named color through Euclidean distance and draws that instead.

When hovering over the graph, actual color from the color space is displayed on
the top as well as the nearest matched color.

![ColorCanvas screenshot](screenshot.png?raw=true "ColorCanvas in action")

## Sample input

Supply a list of colors and their names in the top text area and press
“Redraw”. Be patient, for 1600 colors the runtime is about 5 minutes, because
internally the named colors array needs to be resorted for every pixel.
A marvel of engineering.

Format for supplying named colors, although names may contain spaces:
```
0xFFEBCD;BlanchedAlmond
0xFFEFD5;PapayaWhip
0xFFF0F5;LavenderBlush
0xFFF5EE;Seashell
0xFFF8DC;CornSilk
0xFFFACD;LemonChiffon
```

## Sample output

After mapping all the color, the tool provides a list of colors that remained
unmatched and did not appear in the final image. It is a simple list of hex
values:

```
0xDC143C
0xC93413
0xC41E3A
0xCC3333
0xE34234
0xEC5800
0xB22222
0xCA3435
```

### Disclaimer

This is a tool for solving a specific problem, so if you find it of any use
whatsoever, feel lucky.
