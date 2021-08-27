<script>
  import Tile from "$lib/Tile.svelte";

  const emissionsData = [
    { x: 1990, y: 2891 },
    { x: 1991, y: 2930 },
    { x: 1992, y: 2846 },
    { x: 1993, y: 2772 },
    { x: 1994, y: 2749 },
    { x: 1995, y: 2709 },
    { x: 1996, y: 2807 },
    { x: 1997, y: 2674 },
    { x: 1998, y: 2699 },
    { x: 1999, y: 2667 },
    { x: 2000, y: 2701 },
    { x: 2001, y: 2742 },
    { x: 2002, y: 2656 },
    { x: 2003, y: 2712 },
    { x: 2004, y: 2714 },
    { x: 2005, y: 2696 },
    { x: 2006, y: 2682 },
    { x: 2007, y: 2637 },
    { x: 2008, y: 2567 },
    { x: 2009, y: 2320 },
    { x: 2010, y: 2409 },
    { x: 2011, y: 2200 },
    { x: 2012, y: 2291 },
    { x: 2013, y: 2242 },
    { x: 2014, y: 2047 },
    { x: 2015, y: 1965 },
    { x: 2016, y: 1847 },
    { x: 2017, y: 1787 },
    { x: 2018, y: 1762 },
    { x: 2019, y: 1701 }
  ]

  const emissionsChart = {
    data: emissionsData,
    axisRanges: { x1: 1990, x2: 2019, y1: 1500, y2: 3000 }
  }
  
</script>

<h1>Climate change statistics</h1>

<p>The official ONS website for data and insights on climate change.</p>

<div class="dashboard">
  <Tile
    topic="Climate and weather"
    title="Rainfall"
    chart={emissionsChart}
    lastUpdated="12 July 2021"
    link="climate-weather"
    size="half-width"
  />

  <Tile
    topic="Emissions"
    title="Carbon dioxide"
    lastUpdated="12 July 2021"
    chart={emissionsChart}
    link="emissions"
    size="half-width"
  />

  <Tile
    topic="Drivers"
    title="To be decided"
    lastUpdated="12 July 2021"
    chart={emissionsChart}
    link="drivers"
    size="one-fourth"
  />

  <Tile
    topic="Impacts"
    title="To be decided"
    lastUpdated="12 July 2021"
    chart={emissionsChart}
    link="impacts"
    size="one-fourth"
  />

  <Tile
    topic="Mitigation"
    title="To be decided"
    lastUpdated="12 July 2021"
    chart={emissionsChart}
    link="mitigation"
    size="one-fourth"
  />

  <Tile
    topic="Adaption"
    title="To be decided"
    lastUpdated="12 July 2021"
    chart={emissionsChart}
    link="adaption"
    size="one-fourth"
  />
</div>

<style>
  h1 {
    margin-bottom: 16px;
  }

  p {
    margin-bottom: 16px;
  }

  .dashboard {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 8px;
  }
</style>