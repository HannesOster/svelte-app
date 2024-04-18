<script>
  let name = "Johannes";
  let age = 29;
  let warning = null;
  const increaseAge = () => {
    age += 1;
  };

  const decreaseAge = () => {
    age -= 1;
  };

  $: uppercase = name.toUpperCase();

  $: if (age > 40) {
    warning = "Zu alt";
  } else {
    warning = "Alles cool";
  }
</script>

<main>
  <h3>Vite + Svelte</h3>
  <p>{name}</p>
  <p>{age}</p>
  <p>{uppercase}</p>
  <button on:click={increaseAge}>Increase Age</button>
  <button on:click={decreaseAge}>Decrease Age</button>
  <p>{warning}</p>
</main>
