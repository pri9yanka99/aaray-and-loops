# aaray-and-loops
an array since an array can hold multiple items and we can easily add, remove, or iterate over them.
// Create a variable to hold your NFTs
const NFTs = [];

// This function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(title, director, genre, releaseYear, rating) {
    const NFT = {
        "title": title,
        "director": director,
        "genre": genre,
        "releaseYear": releaseYear,
        "rating": rating
    };
    NFTs.push(NFT);
    console.log("Minted NFT for movie: " + title);
}

// Create a "loop" that will go through an "array" of NFTs
// and print their metadata with console.log()
function listNFTs() {
    for (let i = 0; i < NFTs.length; i++) {
        console.log("\nID:\t\t" + (i + 1));
        console.log("Title: \t\t" + NFTs[i].title);
        console.log("Director: \t" + NFTs[i].director);
        console.log("Genre: \t\t" + NFTs[i].genre);
        console.log("Release Year: \t" + NFTs[i].releaseYear);
        console.log("Rating: \t" + NFTs[i].rating);
        console.log('------------------------');
    }
}

// Print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log("\nTotal NFTs minted: " + NFTs.length);
}

// Call your functions below this line
mintNFT("Inception", "Christopher Nolan", "Sci-Fi", 2010, "8.8");
mintNFT("The Matrix", "Lana Wachowski, Lilly Wachowski", "Action", 1999, "8.7");
mintNFT("Interstellar", "Christopher Nolan", "Sci-Fi", 2014, "8.6");
mintNFT("The Shawshank Redemption", "Frank Darabont", "Drama", 1994, "9.3");
mintNFT("The Godfather", "Francis Ford Coppola", "Crime", 1972, "9.2");

console.log("Listing all NFTs:");
listNFTs();
getTotalSupply();
