<script>
  import * as Pancake from '@sveltejs/pancake';

  export let topic;
  export let title;
  export let lastUpdated;
  export let chart;
  export let size;
  export let link;

  const points = chart.data
</script>

<div class="tile {size}">
    <h2>{topic}</h2>
    <h1>{title}</h1>
    <p>Latest data provided on {lastUpdated}</p>

    <!-- <img src="/static/images/charts/{link}.svg" alt="Chart for {title} in the UK" /> -->

    <div class="chart">
      <Pancake.Chart x1={1990} x2={2019} y1={1500} y2={3000}>
        <Pancake.Box x2={10} y2={100}>
          <div class="axes"></div>
        </Pancake.Box>
        
        <Pancake.Grid vertical count={5} let:value>
          <span class="x label">{value}</span>
        </Pancake.Grid>
    
        <Pancake.Grid horizontal count={0} let:value let:first>
          <span class="y label">{value}</span>
        </Pancake.Grid>
    
        <Pancake.Svg>
          <Pancake.SvgLine data={points} let:d>
            <path class="data" {d}/>
          </Pancake.SvgLine>
        </Pancake.Svg>
      </Pancake.Chart>
    </div>

    <a href="{link}">All {topic} data</a>
</div>

<style>
  .tile {
    background: #f8f8f8;
    border: 1px solid #f3f2f1;
    box-sizing: border-box;
    padding: 16px;
  }

  h2 {
      font-family: "GDS Transport Light";
      font-weight: 400;
      font-size: 19px;
      line-height: 24px;
      color: #6B7276;
  }

  h1 {
      font-family: "GDS Transport Bold";
      font-weight: 700;
      font-size: 24px;
      line-height: 32px;
      margin-bottom: 8px;
  }

  p {
      font-size: 14px;
      line-height: 24px;
      color: #6B7276;
      margin-bottom: 16px;
  }

  img {
    width: 100%;
    margin-bottom: 24px;
  }

  a {
      text-decoration: none;
      font-family: "GDS Transport Bold";
      font-weight: 700;
      font-size: 16px;
  }

  a:hover {
      color: #003078;
  }
  
  .full-width {
    grid-column: 1 / 5;
  }

  .three-fourth {
    grid-column: span 3;
  }

  .half-width {
    grid-column: span 2;
  }

  .one-fourth {
    grid-column: span 1;
  }

  .chart {
		height: 256px;
    padding: 0 16px 40px 16px;
		box-sizing: border-box;
	}
	
	.axes {
		width: 100%;
		height: 100%;
		border-left: 1px solid black;
		border-bottom: 1px solid black;
	}

  .label {
    font-size: 10px;
    color: #6B7276;
  }

	.y.label {
		position: absolute;
		left: -2.5em;
		width: 2em;
		text-align: right;
		bottom: -0.5em;
	}

	.x.label {
		position: absolute;
		width: 4em;
		left: -2em;
		bottom: -22px;
		font-family: sans-serif;
		text-align: center;
	}

	path.data {
		stroke: #383F43;
		stroke-linejoin: round;
		stroke-linecap: round;
		stroke-width: 2px;
		fill: none;
	}
</style>