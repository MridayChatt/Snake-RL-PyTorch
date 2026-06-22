# Snake RL — Deep Q-Learning with PyTorch

An autonomous Snake agent trained using Deep Q-Learning (DQN). Built with PyTorch and Pygame.

## Architecture
- **State:** 11-dimensional vector (danger ahead/left/right, current direction, food location)
- **Model:** Linear Q-Network (11 → 256 → 3)
- **Memory:** Experience replay with batch size 1000
- **Exploration:** Epsilon-greedy decay

## Setup
```bash
pip install pygame torch numpy matplotlib
```

## Run
```bash
# Train the AI
python agent.py

# Play manually
python snake_game_human.py
```

## Files
| File | Description |
|------|-------------|
| `agent.py` | DQN agent — state, memory, action |
| `model.py` | Neural net + Q-trainer |
| `game.py` | Snake environment (Pygame) |
| `helper.py` | Live score plotting |
| `snake_game_human.py` | Human-playable version |