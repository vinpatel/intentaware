+++
title = "Pricing Calculator"
description="Get an Estimate of Our Services"
+++
<script>
function calculatePrice(myform){

  //Get selected data
  var elt = document.getElementById("memoryItem");
  var memory = elt.options[elt.selectedIndex].value;

  var elt = document.getElementById("hddItem");
  var hdd = elt.options[elt.selectedIndex].value;

  var elt = document.getElementById("networkItem");
  var network = elt.options[elt.selectedIndex].value;

  //convert data to integers
  memory = parseInt(memory);
  hdd = parseInt(hdd);
  network = parseInt(network);

  //calculate total value
  var total = (memory*0.02)+hdd+network;

  //print value to  PicExtPrice
  document.getElementById("PicExtPrice").value=total;

}
</script>

<FORM Name="myform">
<SELECT NAME="memoryItem" onChange="calculatePrice()" id="memoryItem">
  <OPTION value="0">Number of Impression or Visits on Digital Asset</OPTION>
  <OPTION value="10000">10000</OPTION>
  <OPTION value="100000">100000</OPTION>
  <OPTION value="1000000">100000</OPTION>
</SELECT>

<SELECT NAME="hddItem" onChange="calculatePrice()" id="hddItem">
  <OPTION value="0">Select One Choice for Support</OPTION>
  <OPTION value="3000">Basic Support Only</OPTION>
  <OPTION value="13000">Innovation Data lab Only</OPTION>
  <OPTION value="16000">Basic Support+Innovation Data Labs</OPTION>
  <OPTION value="20000">Enterprise Support</OPTION>
</SELECT>

<SELECT NAME="networkItem" onChange="calculatePrice()" id="networkItem">
  <OPTION value="0">Select One Choice for Deployment</OPTION>
  <OPTION value="1000">Cloud Based</OPTION>
  <OPTION value="2000">On Premise</OPTION>
  <OPTION value="5000">Hybrid Cloud</OPTION>
</SELECT>
</FORM>
<!--<button type="button" onclick="calculatePrice()">Calculate</button>-->

The estimated cost of services :<INPUT type="text" id="PicExtPrice" Size=8>
