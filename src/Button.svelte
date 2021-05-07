<script>
    import Icon from "./Run.svelte";

    export let icon = false;
    export let label = "";
    export let backgroundColor = "white";
    export let color = "#363636";
    export let size = "medium";
    export let borderStyle = "solid";
    export let borderColor = "#dbdbdb";

    let iconOnly = (icon !== false && label === '') ? true : false;
    let labelOnly = (label !== '' && icon === false) ? true : false;

</script>

<div
    class="button {size}"
    style="background-color: {backgroundColor}; color: {color}; border-style: {borderStyle}; border-color: {borderColor};"
>
    {#if icon}
        <span class="material-icons icons {size}" class:icon-only={iconOnly}>{icon}</span>
    {/if}
    {#if label !== ""}
        <span class="label">{label}</span>
    {/if}
</div>

<style>
    .button {
        display: inline-flex;
        border-width: 1px;
        cursor: pointer;
        justify-content: center;
        text-align: center;
        white-space: nowrap;
        padding: .6rem;
    }
    .icons,
    .label {
        display: inline-flex;
        align-items: center;
        justify-content: center;
    }
    .icons{
        margin-right: .3rem;
    }
    .label{
        padding-bottom: 2px;
    }
    .icon-only{
        margin-left: 0 !important;
        margin-right: 0 !important;
    }
    .large {
        border-radius: 0.7rem;
        font-size: 1.3rem;
        font-weight: 500;
        letter-spacing: 0.1rem;
    }
    .medium {
        border-radius: 0.5rem;
        font-size: 1rem;
        font-weight: 400;
    }
    .small {
        border-radius: 0.3rem;
        font-size: 0.75rem;
        font-weight: 400;
    }
</style>
