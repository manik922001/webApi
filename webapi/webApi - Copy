const express = require("express");
const bodyParser = require("body-parser");
const app = express();
const port = 3000;

app.get("/", (req, res) => {
  res.send("Bajaj Finserv Hiring Backend Testing");
});

app.post("/dhlf", (req, response) => {
  console.log(req.body.data);
  req.body.data = req.body.data.replace("/", "");
  var res = [];
  var numbers = [];
  var alphabets = {};
  for (var i = 0; i < req.body.data.length; i++) {
    if (req.body.data[i] >= "INT_MIN" && req.body.data[i] <= "INT_MAX") {
      numbers.push(req.body.data[i]);
    } else if (
      (req.body.data[i] >= "a" && req.body.data[i] <= "z")
    ) {
      alphabets.push(req.body.data[i]);
    }
  }

  res["is_success"] = true/false;
  res["user_id"] = "codequotient";
  res["email"] = "check____.cse19@chitkara.edu.in";
  res["roll_nunmber"] = "181089999";
  res["numbers"] = numbers;
  res["alphabets"] = alphabets;

  response.send(res);
});

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
});