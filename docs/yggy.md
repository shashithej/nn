---
title: yggy
description: gygygy

---
    <center><div id="numerologyCalcForm">
    <h3>Enter your Date of Birth</h3>
    <form id="numeroCalc">
    <input type="text" oninput="calculateNumber()" id="day" value="" maxlength="2" placeholder="Day">
      <select id="month" value="" onchange="calculateNumber()">
        <option value="0">Select&#8230;</option>
        <option value="1">January</option>
        <option value="2">February</option>
        <option value="3">March</option>
        <option value="4">April</option>
        <option value="5">May</option>
        <option value="6">June</option>
        <option value="7">July</option>
        <option value="8">August</option>
        <option value="9">September</option>
        <option value="10">October</option>
        <option value="11">November</option>
        <option value="12">December</option>
      </select>
      <input type="text" oninput="calculateNumber()" id="year" value="" maxlength="4" placeholder="Year">
    </form>
      <div id="outputText"><h3></h3></div>
    <button id="btnToStore" onclick="directNumerology()" disabled="">Get Free Report</button>
    </div>
    <script>var theForm = document.forms["numeroCalc"];
    var day = theForm.elements["day"];
    var month = theForm.elements["month"];
    var year = theForm.elements["year"];
    var birthNumber = 0;
    function calculateNumber()
    {
      //Instantiate Variables.
      theForm = document.forms["numeroCalc"];
      day = theForm.elements["day"];
      month = theForm.elements["month"];
      year = theForm.elements["year"];
      
      if (validate(day, month, year))
      {
        // Calculate Birth Number.
        birthNumber = calcString(day.value)+calcString(month.value)+calcString(year.value);
        birthNumber = calcString(birthNumber.toString());
         
        document.getElementById("outputText").innerHTML = "<h3>Your Numerology Number is: " + birthNumber + "</h3>";
        document.getElementById("btnToStore").disabled = false;
     
        }
      else
      {
          document.getElementById("btnToStore").disabled = true;
          document.getElementById("outputText").innerHTML = "";
        document.getElementById("outputText").innerHTML = "<h3></h3>";
      }
    }
    
    // Checks if int value of string is greater than 9.
    // If so, it passes to be calculated sequentially.
    function calcString(strValue)
    {
      while (parseInt(strValue) > 9)
        {
          strValue = addStringSequentially(strValue)
        }
      return parseInt(strValue);
    }
    
    // Calculates value of string based on int value.
    function addStringSequentially(strNum)
    {
      
      var placeholder = 0;
      for(var i=0; i<strNum.length; i++)
        {
          placeholder += parseInt(strNum.charAt(i));
        }
      return placeholder.toString();
    }
    
    function validate(day, month, year)
    {
      var dayVal = false;
      var monthVal = false;
      var yearVal = false;
      if(!isNaN(parseInt(day.value)) &#038;&#038; parseInt(day.value) <= 31 &#038;&#038; parseInt(day.value) >=1)
        {
          day.style.backgroundColor = "#eee";
          dayVal = true;
        }else{
          if(day.value == ""){day.style.backgroundColor = "#eee";}
          else{day.style.backgroundColor = "rgba\(255,0,0,0.1\)";}
          day.innerHTML = "Please enter a valid birth date";
        }
      
      if(!isNaN(parseInt(year.value)) && parseInt(year.value) <= (new Date().getFullYear()) &#038;&#038; parseInt(year.value) >=1900)
        {
          year.style.backgroundColor = "#eee";
          yearVal = true;
        }else{
          if(year.value == ""){year.style.backgroundColor = "#eee";}
          else{year.style.backgroundColor = "rgba\(255,0,0,0.1\)";}
          year.innerHTML = "Please enter a valid birth date";
        }
      
      if(parseInt(month.value) != 0)
        {
          monthVal = true;
        }
      
      if (dayVal && monthVal && yearVal)
        {
          return true;
        }
    
      return false;
    }
    
    function directNumerology()
    {
      window.location="https://42437gp20bk7mbq53jjf6kgl4b.hop.clickbank.net/?tid=G";
    }</script></center>