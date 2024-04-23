# Cache Remapping Project - README

## Introduction
This repository contains the codebase and report for the CS204 project aimed at understanding cache misses and proposing a solution to increase Instruction Per Cycle. The project focuses on implementing novel cache remapping strategies to improve cache performance.



## Project Objective
The objective of this project is to reduce conflict misses in the cache by implementing different cache remapping strategies and evaluating their impact on cache performance.

## Versions and Results

### Version 1
- Implemented a cache remapping strategy based on access frequency of cache sets.
- Reserved a least frequently accessed cache set for each hot set.
- Increased IPC by 0.05% from the original result.

### Version 2
- Increased the number of reserved cold sets for each hot set.
- Introduced read redirection to reduce frequent main memory accesses.
- Increased IPC by 0.23% from the original result.

### Version 3
- Rectified logical flaws in determining hot and cold sets.
- Optimized read redirection by removing unnecessary sets.
- Increased IPC by 1.2% from the original result.

## How to Run Instructions
1. Clone the repository:

   ```
   git clone https://github.com/kushrm2803/ChampSim.git
   ```

2.  Open in UNIX based system and navigate to the directory containing the codebase.

3.  For granting permissions, run for both build_champsim.sh and run_champsim.sh

    ```
    chmod +x script.sh                             example :     chmod +x build_champsim.sh
    ```

    ```
    sed -i -e 's/\r$/\n/' script.sh                example:      sed -i -e 's/\r$/\n/' build_champsim.sh
    ```

3. Build the ChampSim simulator:

   ```
   ./build_champsim.sh bimodal no no no no lru 1
   ```

4. Run the ChampSim simulator with the desired configuration:

   ```
   ./run_champsim.sh bimodal-no-no-no-no-lru-1core 1 10 <trace_file_name>
   ```

   Replace `<trace_file_name>` with the name of the trace file you want to simulate.

## References
- Computer Organization and Embedded Systems by Carl Hamacher
- ChampSim simulator: [GitHub](https://github.com/ChampSim/ChampSim)

## Contributors

- [Dhruv Gupta](https://github.com/dhruvgupta2112) - Roll No: 2022CSB1079
- [Kush Mahajan](https://github.com/kushrm2803) - Roll No: 2022CSB1089
- [Nishant Patil](https://github.com/Nishant984) - Roll No: 2022CSB1097

---