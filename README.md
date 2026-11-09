# LLM Waypoint Navigation

A small ROS 2 application that turns natural-language mission requests into
waypoint updates and coordinates navigation actions. It includes a mission
planner, a waypoint manager, named destinations, and waypoint data.

## Files

- `llm_mission_planner.py`: parses mission requests and produces waypoint updates
- `waypoint_manager.py`: monitors waypoint data and coordinates robot navigation
- `named_destinations.yaml`: labels for configured destination poses
- `waypoints.json`: waypoint queue/state data

## Local setup

The scripts expect a ROS 2 workspace containing the `robot_navigation` package.
Adjust the workspace and configuration paths in the scripts for your installation.
Install the ROS 2 dependencies used by the scripts before running them.

Configure any language-model provider credentials through a local environment or
secret manager. Never place API keys in source files or commit local credential
files.

Review waypoint coordinates and destination labels before publishing them; they
may reveal information about a real environment.
