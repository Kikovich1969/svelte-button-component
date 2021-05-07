<script>
  import Button from "./Button.svelte";
  let button = {
    icon: "account_circle",
    size: "large",
    label: "User",
    disabled: true,
    fullWidth: true,
  };
</script>

<svelte:head>
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet" />
</svelte:head>

<main>
  <Button {...button} />
  <Button
    icon="lock"
    color="white"
    backgroundColor="maroon"
    size="medium"
    label="Sperren"
    fullWidth={true}
    disabled={true}
  />
  <Button
    icon="local_fire_department"
    color="white"
    backgroundColor="maroon"
    size="large"
    disabled={true}
  />
  <Button color="white" backgroundColor="black" size="medium" label="Help!" disabled={true} />
  <Button label="Set" size="small" disabled={true} />
  <Button label="Close" size="small" />
  <Button label="Open" size="small" />
  <Button label="Set" size="large" />
  <Button label="Close" />
  <Button label="Open" />
  <Button label="Shit" fullWidth={true} size="large" />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
