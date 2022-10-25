---
Layout:
Title: " Simon Game Demo"
Date: "2022 10 21"
---

# Introduction
Today we had presantation with Moral

# Body 
We were struggling with the simon game and Moral did a prasantion to us on how we were supposed to do it :

import React, { useEffect, useState } from "react"; 

import "./App.css"; 

const App = () => {

     const [pads, setPads] = useState([ { audio: '' , color: "red", flickColor: "white", isChange: false }, { color: "blue", flickColor: "white", isChange: false }, { color: "green", flickColor: "white", isChange: false }, { color: "yellow", flickColor: "white", isChange: false }, { color: "orange", flickColor: "white", isChange: false }, { color: "purple", flickColor: "white", isChange: false }, ]); 

     const [computerMoves, setComputerMoves] = useState([]); 

     const [playerMoves, setPlayerMoves] = useState([]); 

     const playGame = (mode) => { 

        if(mode === 'win'){ var randomNumber = Math.floor(Math.random() * 6) var computerMovesCopy = [...computerMoves, randomNumber] setComputerMoves(computerMovesCopy); 

        }

         if(mode === 'lost'){ var computerMovesCopy = [...computerMoves] setComputerMoves(computerMovesCopy); 

         }

# Conclusion
I am also going to try the simon game .