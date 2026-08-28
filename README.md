# Parkfield Family Atlas — Broad N waveform data

This companion repository stores browser-ready waveform shards for the **Broad N** population in the [Parkfield Family Atlas](https://gemini-lv.github.io/parkfield-family-atlas/).

- 21,120 relaxed two-station neighboring-event communities
- 90,584 community memberships
- 452,920 fixed-UTC station traces (five stations per membership)
- 45 s per trace at 20 Hz
- 212 compressed, on-demand waveform shards

The Broad N population requires support at at least two stations, a displayed median similarity of at least `0.50`, and no more than `1.0 s` of inter-station timing spread. It can include neighboring earthquakes rather than strict repeaters. A single event-level consensus shift is reused at every station.

This is a results-only data repository. It does not contain the discovery implementation. The complete searchable interface, caveats, and catalog annotations are provided by the main atlas.
