<script>
</script>

<h2>US birthrate by year</h2>

<div class="chart" bind:clientWidth={width} bind:clientHeight={height}>
  <svg>
    <g class="axis y-axis">
      {#each yTicks as tick}
        <g class="tick tick-{tick}" transform="translate(0, {yScale(tick)})">
          <line x2="100%" />
          <text y="-4">{tick} {tick === 20 ? ' per 1,000 population' : ''}</text>
        </g>
      {/each}
    </g>

    <g class="axis x-axis">
      {#each points as point, i}
        <g class="tick" transform="translate({xScale(i)},{height})">
          <text x={barWidth / 2} y="-4">{width > 380 ? point.year : formatMobile(point.year)}</text>
        </g>
      {/each}
    </g>

    <g class="bars">
      {#each points as point, i}
        <rect
          x={xScale(i) + 2}
          y={yScale(point.birthrate)}
          width={barWidth - 4}
          height={yScale(0) - yScale(point.birthrate)}
        />
      {/each}
    </g>
  </svg>
</div>

<style>
 h2 {
   text-align: center;
 }

 .chart {
   width: 100%;
   max-width: 500px;
   margin: 0 auto;
 }

 svg {
   position: relative;
   width: 100%;
   height: 200px;
	}

	.tick {
		font-family: Helvetica, Arial;
		font-size: 0.725em;
		font-weight: 200;
	}

	.tick line {
		stroke: #e2e2e2;
		stroke-dasharray: 2;
	}

	.tick text {
		fill: #ccc;
		text-anchor: start;
	}

	.tick.tick-0 line {
		stroke-dasharray: 0;
	}

	.x-axis .tick text {
		text-anchor: middle;
	}

	.bars rect {
		fill: #a11;
		stroke: none;
		opacity: 0.65;
	}
</style>
