# finite (v0.1.0)

**finite** is a [Typst](https://github.com/typst/typst) package for rendering finite automata on top of [CeTZ](https://github.com/johannes-wolf/typst-canvas).

## Usage

For Typst 0.6.0 or later, import the package from the typst preview repository:

```js
#import "@preview/finite:0.1.0": automaton
```

After importing the package, simply call `#automaton()` with a dictionary holding a transition table:
```js
#import "@preview/finite:0.1.0": automaton

#automaton((
  q0: (q1:0, q0:"0,1"),
  q1: (q0:(0,1), q2:"0"),
  q2: (),
))
```

The output should look like this:
![Example for a finite automaton drawn with finite](assets/example.png)

## Further documentation

See `manual.pdf` for a full manual of the package.

## Development

The documentation is created using [Mantys](https://github.com/jneug/typst-mantys), a Typst template for creating package documentation.

To compile the manual, Mantys needs to be available as a local package. Refer to Mantys' manual for instructions on how to do so.

## Changelog

### Version 0.3.0

- Bumped tools4typst to v0.3.2.
- Added `#powerset` command, to transform a NFA into a DFA.
- Added `utils.transpose-table` and `utils.get-inputs` utilities.

### Version 0.2.0

- Bumped CeTZ to v0.1.1.

### Version 0.1.0

- Initial release submitted to [typst/packages](https://github.com/typst/packages).
