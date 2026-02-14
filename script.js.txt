fetch("http://localhost:3000/movies")
.then(res => res.json())
.then(data => {
    const container = document.getElementById("movie-list");
    data.forEach(movie => {
        const img = document.createElement("img");
        img.src = movie.image;
        container.appendChild(img);
    });
});

