<script>
    export let title;
</script>

<div class="chart">
    <h1>{ title }</h1>
    <div class="chart-description">
        <slot></slot>
    </div>
</div>

<style>
    h1 {
        font-size: 24px;
        line-height: 32px;
        margin-bottom: 16px;
    }

    .chart {
        background: #F8F8F8;
        padding: 24px;
    }

    .chart-description {
        font-size: 16px;
        line-height: 24px;
        color: #6B7276;
        max-width: 560px;
    }
</style>