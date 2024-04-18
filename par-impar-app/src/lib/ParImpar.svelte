<script>
  export let number = 0;
  let result;
$: if (number === 0) {
 result = "neutro"
} else {
  if(number % 2 === 0){
    result = "par"
  } else {
    result = "impar"
  }
}
</script>

<p> El número {number} da como resultado {result}</p>

<style>
P {
  Color: rgb(0, 132, 255);
  font-size: 25px;
  font-weight: 500;
}
</style>
