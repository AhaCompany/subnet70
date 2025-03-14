# Vericore Development Guide

## Commands
- Run Perplexity miner: `python -m miner.perplexity.miner --wallet.name bittensor --wallet.hotkey miner_hotkey --subtensor.network ws://127.0.0.1:9944 --axon.port 8901 --netuid 70`
- Run OpenAI miner: `python -m miner.openai.miner_openai --wallet.name bittensor --wallet.hotkey miner_hotkey --subtensor.network ws://127.0.0.1:9944 --axon.port 8901 --netuid 70 --model gpt-4o`
- Run validator API server: `python -m validator.api_server`
- Run validator daemon: `python -m validator.validator_daemon`
- Install dependencies: `pip install -r requirements.txt`
- Lint: `black . && isort . && flake8`

## Code Style
- Use type hints for all function parameters and return values
- Indentation: 4 spaces
- Line length: 100 characters
- Use dataclasses for structured data
- Format imports with isort (stdlib, third-party, local)
- Use bittensor logging patterns for consistency
- Error handling: Use try/except with specific exceptions
- Naming: snake_case for variables/functions, PascalCase for classes

## Architecture
- Miners gather evidence (perplexity miner implementation)
- Validators verify claims via API server and daemon process
- Shared components for logging and protocol definitions