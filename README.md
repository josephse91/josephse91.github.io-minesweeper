# Minesweeper

Interactive version of minesweeper

[Live Minesweeper](https://josephse91.github.io/minesweeper_project/ "Minesweeper")

## Technologies Used

- Javascript
- React
- CSS

## Highlighted Features

**State Management**

By lifting the state of an `updateGame` function to the Tile component, I used a click event handler on each tile to give it the capability to setState and update the board

```
 ./components/tile.jsx

 handleClick(e) {
    const flagged = e.altKey ? true : false;
    this.props.updateGame(this.props.tile, flagged);
  }
```

```
 ./components/game.jsx

 updateGame(tile, flagged) {
    if (flagged) {
      tile.toggleFlag();
    } else {
      tile.explore();
    }

    this.setState({ board: this.state.board });
  }
```

**Object Oriented Principles**

The logic of the game was coding with Object Oriented Programming principles. A tile class and board class was created and imported into the game jsx. file.

## Run Locally

Clone the project

```bash
git clone https://github.com/josephse91/minesweeper_project
```

Go to the project directory

Install dependencies

`NOTE`: This app was created using npm version v14. To avoid conflict, it would be beneficial to install npm version 14.

```bash
  npm install
```
