# Langtron's Ant

This program simulates Langton's ant, a two-dimensional universal Turing machine characterized by a simple rule set that produces complex emergent behavior, as designed by Christopher Langton in 1986. The simulation features a customizable board, ant movement with optional obstacles.

## Prerequisites

- GCC Compiler

## Compilation

To compile the program, navigate to the directory containing the source code files and execute the following command:

```bash
cc -o ant_simulation -std=c11 main.c ant_simulation.c board.c display.c input.c saving_to_file.c 
```

## Usage

You can run the program using the following command:

```bash
./ant_simulation <rows> <columns> <iterations> <name_prefix> <initial_direction> -o <obstacle_percentage> -f <map_filename>
```

Where:

- `<rows>`: The number of rows in the board.
- `<columns>`: The number of columns in the board.
- `<iterations>`: The number of moves for the ant.
- `<name_prefix>`: Prefix for files that will store the generated boards.
- `<initial_direction>`: The starting direction of the ant, which can be 'N' (North), 'S' (South), 'E' (East), or 'W' (West).
- `<obstacle_percentage>`: The percentage of the board that will contain obstacles. If omitted, no obstacles will be created.
- `<map_filename>`: The name of the file from which the board will be loaded. If this is not specified, a random board will be generated.

## Example

```bash
./ant_simulation 10 10 215 test N
```

This command runs a simulation on a 10x10 board for 215 iterations. The generated files will have the prefix "file," the ant will begin facing North.

```bash
git config --global user.name nesterova-p
```

## Result

### Iteration 1
```
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ▲ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
```

### Iterating in the middle of the program running 
```
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ░ ░ ░ ░ ░
░ ░ ░ ░ ░ ◀ ░ █ ░ ░
░ ░ ░ ░ ░ ░ █ ░ █ ░
░ ░ ░ ░ █ ░ ░ ░ █ ░
░ ░ ░ █ ░ ░ ░ █ ░ ░
░ ░ █ ░ ░ █ ░ ░ ░ ░
░ ░ █ ░ ░ █ ░ ░ ░ ░
░ ░ ░ █ ░ ░ █ ░ ░ ░
░ ░ ░ ░ █ █ ░ ░ ░ ░
```

### Iteration 215
```
░ █ █ █ ░ ░ ░ ░ █ ░
░ █ █ █ █ █ █ █ █ ░
░ ░ █ █ ░ █ ░ ░ █ ░
░ ░ █ ░ ░ ░ █ ░ █ █
░ █ ░ ░ █ █ ░ █ █ █
█ ▶ █ ░ ░ ░ ░ ░ █ ░
█ █ ░ ░ █ █ █ █ ░ ░
```
