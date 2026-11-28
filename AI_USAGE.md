# AI usage

## Setup

- Tool used: OpenAI Codex.
- Delegated tasks: Reviewed the assignment, proposed a work plan, and created the starter notebooks and project documentation.
- Example: Codex wrote the Q2 loading cell using a relative path and the supplied CSV's exact filename.
- Verification: Codex executed the loading cell from the project folder and compared the resulting dimensions with a separate read of the CSV.

## Q1A regular firing

- Codex implemented the agreed 100 ms interval and 50 ms start time using NumPy's `arange`.
- Codex ran the notebook's Python cells and checked the spike count, recording bounds, first and last spike times, and all intervals between adjacent spikes.

## Q1A irregular firing

- Codex chose independent exponential waiting times with a mean of 0.10 seconds and implemented the simulation. Seed 42 produced 60 spikes.
- Codex checked that repeating seed 42 reproduced the timestamps and that a zero-length recording returned no spikes. Across 1,000 seeds, every spike train stayed ordered and inside the five-second window, with an average of 50.031 spikes per recording.

## Q1A bursting firing

- Tool used: Claude Code (Claude Opus).
- Claude proposed three designs. I chose fixed bursts of five spikes 10 ms apart, with random quiet gaps between bursts. I then chose a quiet gap of 0.10 seconds plus an exponential wait averaging 0.36 seconds, over a uniform or normal gap. A normal gap can produce tiny or negative gaps that merge bursts. I also agreed that the recording starts with a quiet gap and that a burst crossing five seconds is cut off.
- Claude implemented `simulate_bursting` and ran the notebook from top to bottom. Seed 42 produced 35 spikes in seven complete bursts.
- Across 1,000 seeds, every spike train was ordered and inside the five-second window, and every burst except possibly the last had five spikes 10 ms apart. No quiet gap was shorter than 0.10 seconds, and 84 recordings ended with a partial burst. The average was 49.255 spikes per recording.
- Long simulations gave a mean quiet gap of 0.4602 seconds (expected 0.46) and a rate of 10.019 spikes per second (expected 10). Repeating a seed reproduced the timestamps, and a zero-length recording returned no spikes.

## Independent review

As the analysis develops, document at least one specific AI-generated assumption, suggestion, or mistake that you challenged, modified, or independently verified. Include the check you performed and its result.
