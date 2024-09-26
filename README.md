# Boggle Solver (Rust + Web Integration)

Welcome to my **Boggle Solver** project, a personal project aimed at demonstrating my proficiency in Rust, algorithms, and web development. This project highlights my ability to work with complex algorithms, optimize solutions for performance, and integrate backend Rust services with a modern web frontend.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Optimizations](#optimizations)
- [Challenges Faced](#challenges-faced)
- [Installation](#installation)
- [Usage](#usage)
- [Future Improvements](#future-improvements)

## Introduction

The **Boggle Solver** is a Rust-based backend that efficiently solves Boggle boards, combined with a web-based frontend that allows users to generate random boards, manually edit them, and see the solution in real-time. This project was designed as part of my portfolio to showcase my skills in algorithm design, Rust programming, and full-stack web development.

## Features

- **Board Generation**: Random Boggle boards can be generated or manually edited by the user.
- **Efficient Solver**: The backend efficiently solves the Boggle board using advanced algorithms (DFS and Trie-based word lookup).
- **Real-Time Feedback**: Results are dynamically displayed on the frontend.
- **Interactive UI**: The user can select words, and the corresponding paths are highlighted on the board.
- **Responsive Design**: The web interface adapts to various screen sizes and devices.

## Tech Stack

- **Rust**: Backend logic for solving the Boggle board.
- **Trie Data Structure**: For efficient word lookup during pathfinding.
- **JavaScript (ES6)**: Handles the frontend logic, including board generation, user interaction, and async API requests.
- **HTML/CSS + Bootstrap**: Provides a responsive and modern user interface.
- **Fetch API**: Facilitates communication between the Rust backend and the web frontend.

## How It Works

### Algorithm Overview

The Boggle Solver uses **Depth-First Search (DFS)** with **backtracking** to explore all valid paths on the board. A **Trie** data structure is employed to ensure efficient word lookups, pruning invalid paths early and reducing the number of unnecessary calculations.

1. **Board Traversal**: The algorithm explores every possible path on the board, visiting adjacent characters to form potential words.
2. **Word Lookup**: Each path is validated using a Trie to check if the current string is a valid word or a prefix of one.
3. **Result Display**: The valid words, along with their corresponding points, are returned to the frontend and displayed in an organized manner.

### Web Integration

The web frontend communicates with the Rust backend using asynchronous API calls:
- **Board Submission**: The frontend sends the generated/edited board to the Rust backend.
- **Solution Response**: The backend returns the valid words found on the board, which are then displayed interactively on the frontend.

## Optimizations

1. **Trie Data Structure**: Optimizes word lookup, reducing time complexity for checking prefixes and complete words.
2. **Pruning**: The algorithm skips invalid paths early using the Trie, which drastically reduces the number of recursive calls.
3. **Memoization**: Redundant calculations are avoided by caching previously computed results.
4. **Parallelization**: Rust's concurrency model allows parts of the board to be processed concurrently, improving performance on multi-core processors.

## Challenges Faced

- **Efficient Traversal**: Optimizing the algorithm to avoid redundant paths and unnecessary recalculations while ensuring accuracy.
- **Integration of Rust with Web Technologies**: Managing cross-language communication (Rust backend with JavaScript frontend) and handling CORS issues during API calls.
- **UI Design**: Ensuring a responsive, user-friendly interface that works across multiple devices and handles real-time updates.

## Installation

To run the Boggle Solver locally, follow these steps:

### Prerequisites

- **Rust**: Make sure you have Rust installed. You can get it from [here](https://www.rust-lang.org/tools/install).
- **Node.js**: To handle the web frontend.

### Clone the Repository

```bash
git clone https://github.com/yourusername/boggle-solver.git
cd boggle-solver
```

### Backend Setup (Rust)

1. Navigate to the Rust project directory:

   ```bash
   cd bogglesolver
   ```

2. Run the Rust server:

   ```bash
   cargo run
   ```

This starts the Rust server on `localhost:8080`.

### Frontend Setup (HTML/JS)

1. Open `boggle.html` in a browser or serve it via a local server:

   ```bash
   open boggle.html
   ```

## Usage

1. Generate a random Boggle board or edit the letters directly.
2. Click **Solve** to send the board to the backend for solving.
3. View the solved words and their paths on the board.
4. Use the accordion feature to collapse/expand results by letter.

## Future Improvements

- **Multi-Language Support**: Add the ability to solve Boggle boards in different languages.
- **Word Definition Lookup**: Integrate a dictionary API to display definitions for found words.
- **Mobile Optimization**: Further improve responsiveness and user interaction on mobile devices.
- **Performance Benchmarking**: Add benchmarking tools to measure the efficiency of the algorithm under various conditions.

---

## License

This project is licensed under the MIT License.

## Contact

If you have any questions or feedback, feel free to contact me at [your-email@example.com].

---

This README gives a detailed overview of your project, emphasizing the skills and knowledge you demonstrated. It’s structured in a professional way and can easily be added to your GitHub repository. Let me know if you need further customization!
