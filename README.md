# TfL Journey Planner

A Python command-line journey planner that uses Dijkstra's algorithm to find the lowest travel-time route through a fixed London Underground graph.

## Run locally

Requires Python 3. No third-party packages or API keys are needed.

```bash
git clone https://github.com/Akrouma03/TFL-Journey-Planner.git
cd TFL-Journey-Planner
python "TFL-Journey-Planner-main/TFL-Journey-Planner-main/TFL Journey Planner.py"
```

Enter the starting and destination station when prompted. For example, try `Waterloo` and `Bank`. The program prints the route and its total travel time in minutes.

Station names are case-sensitive and must match the names in the source exactly. Unrecognised names produce `error`.

## How it works

1. Represent stations as graph nodes and connections as weighted edges.
2. Start with a distance of zero at the origin.
3. Repeatedly visit the unvisited station with the smallest known distance and update its neighbours.
4. Follow the recorded predecessors back from the destination to reconstruct the route.

## Scope and limitations

This is an algorithm demonstration using hard-coded station names and travel times. It does not query live TfL services or account for current disruptions, timetables or accessibility requirements. Some station names reflect the original dataset rather than current naming.

The original source and license are in [the project folder](TFL-Journey-Planner-main/TFL-Journey-Planner-main/).