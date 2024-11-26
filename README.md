# 📦 Bellande Node Importance Models & Executables

# Demo of Bellande Node Importance
![Demo GIF](executable/bellande_node_importance.gif)

## 🧙 Organization Website
- [![Organization Website](https://img.shields.io/badge/Explore%20Our-Website-0099cc?style=for-the-badge)](https://robotics-sensors.github.io)

## 🧙 Organization Github
- [![Organization Github ](https://img.shields.io/badge/Explore%20Our-Github-0099cc?style=for-the-badge)](https://github.com/Robotics-Sensors)

# Author, Creator and Maintainer
- **Ronaldson Bellande**

## Usage
```
./Bellande_Node_Importance passcode node recent_nodes important_nodes adjacent_segments grid_steps min_segment_coverage
```

### Arguments
1. `passcode`: The access key (must be "bellande_node_importance_executable_access_key")
2. `node`: Node to evaluate as [coordinates, segment] (e.g., "[[5.0, 5.0, 5.0], 1]")
3. `recent_nodes`: List of recent nodes as [[coordinates, segment], ...] (e.g., "[[[4.0, 4.0, 4.0], 1], [[6.0, 6.0, 6.0], 1]]")
4. `important_nodes`: Dictionary of important nodes by segment (e.g., "{'1': [[[4.0, 4.0, 4.0], 1]], '2': [[[15.0, 15.0, 15.0], 2]]}")
5. `adjacent_segments`: Dictionary of adjacent segments (e.g., "{'1': [2], '2': [1]}")
6. `grid_steps`: Step sizes for each dimension as a list (e.g., "[10.0, 10.0, 10.0]")
7. `min_segment_coverage`: Float value for minimum segment coverage ratio (default: 0.5)

### Example
```bash
./Bellande_Node_Importance \
"bellande_node_importance_executable_access_key" \
"[[5.0, 5.0, 5.0], 1]" \
"[[[4.0, 4.0, 4.0], 1], [[6.0, 6.0, 6.0], 1], [[5.5, 5.5, 5.5], 1]]" \
"{'1': [[[4.0, 4.0, 4.0], 1]], '2': [[[15.0, 15.0, 15.0], 2]]}" \
"{'1': [2], '2': [1]}" \
"[10.0, 10.0, 10.0]" \
"0.5"
```

### Notes
- Passcode must be exactly "bellande_node_importance_executable_access_key"
- All coordinates within nodes must have the same dimensions
- Grid steps must match the dimensionality of the nodes
- Use proper Python list and dictionary syntax for all inputs
- The script supports infinite dimensions, limited only by system resources
- All numeric values can have decimal precision
- The function evaluates node importance based on:
  - Coverage ratio in the segment
  - Connection potential with important nodes in adjacent segments
  - Local neighbor density

### Error Handling
The script includes error handling for:
- Incorrect number of arguments
- Invalid passcode
- Mismatched dimensions across coordinates
- Invalid input format (syntax errors)
- Invalid data structure formats
- Inconsistent dimensionality between nodes and grid steps
- Other unexpected errors

## License
This Algorithm or Models is distributed under the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/), see [LICENSE](https://github.com/RonaldsonBellande/bellande_node_importance_models/blob/main/LICENSE) and [NOTICE](https://github.com/RonaldsonBellande/bellande_node_importance_models/blob/main/LICENSE) for more information.
