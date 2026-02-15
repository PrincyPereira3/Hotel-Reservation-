<!DOCTYPE html>
<html>
<head>
  <title>Hotel Reservation System</title>
  <style>
    body { font-family: Arial; text-align:center; }
    .floor { margin:10px; }
    .room {
      display:inline-block;
      width:50px;
      height:50px;
      margin:4px;
      line-height:50px;
      border-radius:6px;
      background:#90caf9;
      cursor:pointer;
    }
    .occupied { background:#ef5350; }
    .selected { background:#66bb6a; }
  </style>
</head>
<body>

<h2>Hotel Room Reservation System</h2>

<input type="number" id="roomCount" min="1" max="5" placeholder="Enter rooms (1-5)">
<button onclick="bookRooms()">Book</button>
<button onclick="randomOccupy()">Random Occupancy</button>
<button onclick="resetAll()">Reset</button>

<h3 id="travelTime"></h3>

<div id="hotel"></div>

<script>

let hotel = {};
let selectedRooms = [];

function generateHotel(){
  const container = document.getElementById("hotel");
  container.innerHTML = "";
  hotel = {};

  for(let f=1; f<=10; f++){
    let floorDiv = document.createElement("div");
    floorDiv.className = "floor";
    floorDiv.innerHTML = "<b>Floor "+f+"</b><br>";

    let roomCount = (f==10)?7:10;
    hotel[f] = [];

    for(let r=1; r<=roomCount; r++){
      let roomNumber = f*100 + r;
      let room = document.createElement("div");
      room.className = "room";
      room.innerText = roomNumber;
      room.dataset.floor = f;
      room.dataset.pos = r;
      floorDiv.appendChild(room);

      hotel[f].push({
        number: roomNumber,
        floor: f,
        pos: r,
        occupied:false
      });
    }

    container.appendChild(floorDiv);
  }
}

function calculateTime(r1, r2){
  let vertical = Math.abs(r1.floor - r2.floor) * 2;
  let horizontal = Math.abs(r1.pos - r2.pos);
  return vertical + horizontal;
}

function getAvailableRooms(){
  let rooms = [];
  for(let f in hotel){
    hotel[f].forEach(r=>{
      if(!r.occupied) rooms.push(r);
    });
  }
  return rooms;
}

function combinations(arr, k){
  let result=[];
  function backtrack(start, path){
    if(path.length===k){
      result.push([...path]);
      return;
    }
    for(let i=start;i<arr.length;i++){
      path.push(arr[i]);
      backtrack(i+1,path);
      path.pop();
    }
  }
  backtrack(0,[]);
  return result;
}

function bookRooms(){
  let count = parseInt(document.getElementById("roomCount").value);
  if(!count || count<1 || count>5) return alert("Enter 1-5 rooms");

  let bestCombo = null;
  let minTime = Infinity;

  // Same floor priority
  for(let f in hotel){
    let available = hotel[f].filter(r=>!r.occupied);
    if(available.length >= count){
      let combos = combinations(available, count);
      combos.forEach(c=>{
        let time = calculateTime(c[0], c[c.length-1]);
        if(time < minTime){
          minTime = time;
          bestCombo = c;
        }
      });
    }
  }

  // Across floors if needed
  if(!bestCombo){
    let available = getAvailableRooms();
    let combos = combinations(available, count);
    combos.forEach(c=>{
      let time = calculateTime(c[0], c[c.length-1]);
      if(time < minTime){
        minTime = time;
        bestCombo = c;
      }
    });
  }

  if(!bestCombo) return alert("Not enough rooms");

  bestCombo.forEach(r=>{
    r.occupied=true;
  });

  visualize();
  document.getElementById("travelTime").innerText =
    "Total Travel Time: "+minTime+" minutes";
}

function visualize(){
  document.querySelectorAll(".room").forEach(div=>{
    div.classList.remove("occupied");
  });

  for(let f in hotel){
    hotel[f].forEach(r=>{
      if(r.occupied){
        document.querySelectorAll(".room").forEach(div=>{
          if(parseInt(div.innerText)==r.number)
            div.classList.add("occupied");
        });
      }
    });
  }
}

function randomOccupy(){
  resetAll();
  let rooms = getAvailableRooms();
  rooms.forEach(r=>{
    if(Math.random() < 0.3){
      r.occupied=true;
    }
  });
  visualize();
}

function resetAll(){
  for(let f in hotel){
    hotel[f].forEach(r=>r.occupied=false);
  }
  visualize();
  document.getElementById("travelTime").innerText="";
}

generateHotel();

</script>

</body>
</html>
