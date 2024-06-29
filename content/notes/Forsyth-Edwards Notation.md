---
title: "Forsyth-Edwards Notation (FEN)"
aliases:
- FEN
---

FEN notation is used for describing a particular board position of a chess game. Purpose of FEN is to provide all the necessary information to restart a game from a particular position.

Explored this notation during the GPU Hackathon in San Francisco

## FEN Fields

Wikipedia Link: https://en.wikipedia.org/wiki/Forsyth–Edwards_Notation

FEN record contains six fields each separated by a space

1. Piece placement data: Each rank is described starting with rank 8 and ending with rank 1, with a "/" between each one. The contents of the square are described from a-file to the h-file. Each piece is identified by a single letter taken from the standard English names (pawn = "P", knight = "N", bishop = "B", rook = "R", queen = "Q", king = "K"). White pieces use uppercase letters while black pieces use lowercase letters. 
2. Active color: "w" means that White is to move; "b" means that Black is to move
3. If neither side has the ability to castle, this field uses the character "-". Otherwise, this field contains one or more letters: "K" if White can castle kingside, "Q" if White can castle queenside, "k" if Black can castle kingside, and "q" if Black can castle queenside. A situation that temporarily prevents castling does not prevent the use of this notation.
4. [[En Passant]] target square: The square over which a pawn has passed while moving 2 squares is given in algebraic notation. If there's no en passant target square the field uses the character "-". An updated version makes it so that it's only recorded if a legal en passant is possible but old version of this standard is most commonly used
5. Halfmove clock: Number of halfmoves since the last capture of pawn advance, used for the [[fifty-move rule]]
6. Fullmove number: The number of full moves. It starts at 1 and is incremented after Black's move
