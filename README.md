# Kicad Notes

## About

I am learning how to use Kicad. I am new to such tools, so I've created this
repo to take notes about what I've learned along the way.

## Notes

1. Components should be aligned to a grid. If they are not, you may run into
issues connecting them. One way to ensure this is to highlight a region of 
components, right click, and choose the "Align Elements to Grid" option.

2. Running the electrical rules check is a crucial step towards uncovering
problems with schematics.

3. Power components (e.g. GND, PWR +5V) must be flagged by creating a PWR_FLAG
component and attaching it to the same net as the power component. This is how
the ERC tool identifies power sources/sinks.

4. Components must be labeled properly to pass the electrical rule check. If
they are not, this often manifests as *two* ERC errors: first, an error saying
that the component is not labeled and second, an error that a wire/component
isn't connected to anything. This must be because the ERC treats the unlabeled
component similarly to just not existing.
