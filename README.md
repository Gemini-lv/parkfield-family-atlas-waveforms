# Parkfield Family Atlas — Broad N waveform data

This companion repository stores browser-ready waveform shards for the **Broad N** population in the [Parkfield Family Atlas](https://gemini-lv.github.io/parkfield-family-atlas/).

- 21,120 relaxed two-station neighboring-event communities
- 90,584 community memberships
- 452,920 fixed-UTC station traces (five stations per membership)
- 45 s per trace at 20 Hz
- 212 compressed, on-demand waveform shards

The Broad N population requires support at at least two stations, a displayed median similarity of at least `0.50`, and no more than `1.0 s` of inter-station timing spread. It can include neighboring earthquakes rather than strict repeaters. A single event-level consensus shift is reused at every station.

## Alignment refinement in release `v2`

Release `v2` re-estimates each non-anchor event's residual display shift directly from the fixed-UTC waveforms. The estimator obtains local lag evidence independently at each available station, then applies one robust cross-station consensus shift to every station trace for that event. It does not shift each station independently.

- 10,435 / 21,120 families have reliable waveform support for every displayed member.
- 43,508 / 69,464 non-anchor memberships have a reliable residual shift supported by at least two stations.
- The median family-level post-alignment high-energy CC is `0.898` across the complete Broad N population.

The atlas keeps the discovery-stage similarity and the post-alignment waveform CC as separate quantities. Members that fail the waveform-consensus check retain the original graph shift and are explicitly labelled `graph shift only`; they must not be interpreted as confirmed aligned repeaters.

This is a results-only data repository. It does not contain the discovery implementation. The complete searchable interface, caveats, and catalog annotations are provided by the main atlas.
