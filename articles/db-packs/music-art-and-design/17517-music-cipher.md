# Music cipher

A music cipher is an algorithm for encrypting a plaintext message into musical symbols or sounds. Music ciphers are related to but distinct from musical cryptograms, which encode names into themes (like the BACH motif) through visual or alphabetical similarities between letters and note names. Music ciphers hide longer messages, and the letter-to-symbol mapping is purely conventional.

The core design problem is arithmetic: a standard alphabet has 26 letters, but a diatonic scale offers only seven pitch names (A through G). Designers solve this by combining pitch with other musical attributes: octave register, rhythmic duration, clef, or accidentals (sharps and flats). One early solution, found in Friar Nicholas Philip's 1432 manuscript, paired five pitches with four durations, producing twenty distinct symbols. The same trade-off shapes every later system.

## Substitution ciphers

Most music ciphers are substitution ciphers, where each letter becomes one symbol. In simple diatonic systems, seven pitches stand in for multiple letters. Giambattista della Porta's 1602 cipher became the most famous: letters A through M (omitting J and K) climbed stepwise up an octave and a half of whole notes, and the remaining letters (omitting V and W) descended using half notes. Because alphabetic and scalar sequences track each other so closely, the cipher is weak and the melodies sound artificial. Variations appear in treatises by Schwenter (1622), Wilkins (1641), Kircher (1650), Schott (1655), and Thicknesse (1772).

Chromatic substitution enlarges the pool by adding sharps and flats to the seven diatonic pitches, yielding twenty-one symbols, still short of twenty-six. The most comprehensive chromatic cipher, attributed to Michael Haydn in 1808, covers thirty-one German letters along with punctuation, parentheses, and word segmentation. Because many of its pitches are enharmonic equivalents (C-sharp and D-flat sound identical on a piano), the message cannot be transmitted as sound; it only works as visual steganography on a page. The resulting melody is also harshly atonal, useless for disguising the message as real music.

## Compound motivic ciphers

Compound motivic ciphers replace each letter with a short motive of two or more notes rather than a single note. In 1804, Johann Bücking published a cipher mapping the alphabet onto a minuet in G major: each letter became a one-measure motive of three to six notes, with extra measures prepended and appended for musical framing. Mozart's KV 516f manuscript (1787) uses a similar technique, generally read as a parlor game rather than a serious cipher.

Friedrich von Öttingen-Wallerstein (around 1600) took a different compound approach modeled on the polybius square. Letters were placed in a 5×5 grid hidden in angel names, and each cell was named not by row-and-column numbers but by the solfège syllables Ut, Re, Mi, Fa, Sol. Each letter thus became a two-note melodic motive. The same design reappears, uncredited, in Gustavus Selenus (1624) and Johann Balthasar Friderici (1665).

## Keys and steganography

Because Öttingen-Wallerstein's grid uses relative solfège degrees rather than fixed pitches, the same melody can be transposed to any key while retaining its meaning. That transposition doubles as a cipher key: the recipient needs to know which key to read. Öttingen-Wallerstein inserted rests as markers to signal when a new key was required. Francesco Lana de Terzi (1670) built a more conventional text-string key on top of a Porta-style cipher, functioning much like a Vigenère cipher.

A more elaborate keyed cipher appears in an anonymous mid-18th-century French manuscript from Port-Lesney. It uses an Alberti cipher disk: two rotating disks with concentric rings of time signatures, letters, compound musical symbols, and three clefs. The recipient aligns the disks using the clef, time signature, and key shown at the head of the staff. At least a dozen variations of this device circulated in French, German, and English through the 18th and 19th centuries.

The modern Solfa Cipher (2013) combines relative solfège degrees with relative metric placement rather than fixed note durations. The output resembles common-practice melody and remains playable after transposition. Keys can also be conveyed by date through a system called Solfalogy. Solfa Cipher has surfaced in music by Twenty One Pilots and The Smile, and as a plot device in novels.

## Encryption and steganography together

Music ciphers typically blend cryptography with steganography. Encryption scrambles a message so it is unreadable; steganography hides it so no one suspects a message exists. Most practitioners believed that disguising text as sheet music gave added security, because intercepted music would rarely be examined for hidden content. As Francesco Lana de Terzi observed, the disguise works not because the cipher melody sounds like real music, but because almost no one is musically literate enough to notice that it does not.
