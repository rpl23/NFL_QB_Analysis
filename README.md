# NFL QB Valuation Analysis This Project is Incomplete

This project analyzes quarterback performance using various metrics to generate comprehensive valuation scores. The analysis combines traditional statistics with advanced metrics to provide a multi-dimensional assessment of quarterback performance.

## Project Structure

```
.
├── Data/
│   ├── Processed/
│   │   └── qb_valuations.csv    # Final QB valuation results
│   └── Raw/
│       ├── pbp_stats.csv        # Play-by-play statistics
│       └── players.csv          # Player information
├── logs/
│   └── qb_valuation.log        # Application logs
├── Notebooks/                   # Jupyter notebooks for analysis
├── Src/
│   └── Data/
│       ├── Features/           # Feature engineering modules
│       ├── __init__.py
│       ├── analyze_qb.py       # QB analysis logic
│       ├── collect_player_stats.py  # Player statistics collection
│       └── process_player_data.py   # Data processing utilities
├── Tests/                      # Test directory
├── venv/                       # Python virtual environment
├── .gitattributes             # Git attributes configuration
├── .gitignore                 # Git ignore rules
├── requirements.txt           # Project dependencies
└── run_processor.py          # Main processing script
```

## Features

The analysis evaluates quarterbacks across multiple dimensions:

- **Basic Statistics**
  - Completion Percentage
  - Yards per Attempt
  - Touchdown Rate
  - Interception Rate
  - Sack Rate

- **Advanced Metrics**
  - Deep Completion Rate
  - Pressure Completion Rate
  - Third Down Conversion Rate
  - Red Zone Touchdown Rate
  - Average EPA (Expected Points Added)

All metrics are provided in both raw and normalized forms to facilitate comparisons across different eras and systems.

## Core Components

- `analyze_qb.py`: Implements the core QB analysis logic
- `collect_player_stats.py`: Handles collection of player statistics
- `process_player_data.py`: Contains data processing utilities
- `run_processor.py`: Main entry point for the analysis pipeline

## Data Files

### Input
- `pbp_stats.csv`: Play-by-play statistics
- `players.csv`: Player information

### Output
- `qb_valuations.csv`: Contains processed QB valuations with the following metrics:
  - GSIS ID and player name
  - Raw and normalized performance metrics
  - Overall value score

## Setup and Usage

1. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Run the analysis:
```bash
python run_processor.py
```

## Development

- Source code is organized in the `Src/Data` directory
- Unit tests are located in the `Tests` directory
- Jupyter notebooks for exploratory analysis are in the `Notebooks` directory

## Logging

The application generates detailed logs in:
- Console output (INFO level and above)
- Log file: `logs/qb_valuation.log`

## Error Handling

The application includes comprehensive error handling and logging to facilitate debugging and maintenance. All major operations are wrapped in try-except blocks with appropriate error messages.
