<script>
  let count = 0;
  let message = '';

  const increment = async () =>
  {
    count += 1;    
  };

  // Fetch data from index.php and update the 'message' variable
  const fetchData = async () =>
  {
    try {
      const response = await fetch('http://localhost'); // Assuming index.php is in the same domain
      const data = await response.text();
      if (response.status === 200 && data.trim() !== '') {
        message = data;
      } else {
        message = 'Error fetching data'; // Display an error message if the request fails or the data is empty
      }
    } catch (error) {
      message = `EXCEPTION: ${error}`; // Display an error message if an exception occurs
    }
  };
  
</script>

<button on:click={increment}>
  Press the button to test Svelte.
</button>
<br>
<p>  
  count is {count}
</p>
<br>
<button on:click={fetchData}>
  Press the button to test the server.
</button>
<br>
<p>{message}</p>
