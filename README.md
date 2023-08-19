# JSReact-TypeScript-HangMan-Workshop-2023
Simple React HangMan Application using React, Vite, and TypeScript

### Website Application Game Called "Hangman".

## Description

This is a website application about guessing words. 
It is a project executed using React.

## Local Installation

1. Clone the repository
2. Run `npm install` in the directory.
\
&nbsp;

## Built With
[![My Skills](https://skillicons.dev/icons?i=js,react,vite,typescript,html,css,vscode)](https://skillicons.dev)

\
&nbsp;

# React Sample Code　

```javascript
type HangmanWordProps = {
    guessedLetters: string[]
    wordToGuess: string
    reveal?: boolean
}


const HangmanWord = ({guessedLetters, wordToGuess, reveal=false}: HangmanWordProps) => {
    
  return (
    <div style={{
        display: 'flex',
        gap: '.25em',
        fontSize: '6rem', fontWeight: 'bold',
        textTransform: 'uppercase',
        fontFamily: 'monospace'
    }}>
      {wordToGuess.split('').map((letter, index) => (
        <span style={{
            borderBottom: '.1em solid black'
        }} key={index}>
            <span style={{
                visibility: guessedLetters.includes(letter) || reveal? 'visible' : 'hidden',
                color: !guessedLetters.includes(letter) && reveal? "red" : "black",
            }}>{letter}</span>
        </span>
      ))}
    </div>
  )
}

export default HangmanWord
```

\
&nbsp;

# Screenshots

### Home Page 
<img src="Screenshots/homepage.jpg" alt="Home page" width="800">

\
&nbsp;

