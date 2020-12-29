---
layout: post
title:  "Responsive Design"
date:   2020-12-10 11:18:12 -0700
categories: Front-end web app
---

Main idea: write codes in the dymanic design so that it is resizable and suitable for different devices. 

Best Practice: 
* Relative Units: auto-resize app depending on which devices sitting on, %, em, rem, vh (viewport height), vw (viewport width). 
* Media Queries: Material UI has media queries. 
* Grid system

How to implement responsive design? 
* Step 1: `import useMediaQuery from "@material-ui/core/useMediaQuery`
* Step 2: set theme and matchesSM. `const theme = useTheme();const matchesSM = useMediaQuery(theme.breakpoints.up('sm'));`. 
* Step 3: set breakpoint. e.g., under grid 
`<Grid item style={{marginTop: matchesSM ? "5em": "3em"}}>`, `matchesSM` is a Bool. So the marginTop changes with `matchesSM`, if `matchesSM` is true, marginTop is 5em, elsewise it is 3em. It can be also used in Grid container. e.g., `<Grid container direction={matchesSM ? "column" : "row"}>`. 