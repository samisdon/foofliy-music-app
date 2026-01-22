import { useState } from "react";

const songsData = [
  { title: "Kesariya", artist: "Arijit Singh" },
  { title: "Apna Bana Le", artist: "Arijit Singh" },
  { title: "Heeriye", artist: "Jasleen Royal" },
  { title: "Chaleya", artist: "Arijit Singh" },
  { title: "Obsessed", artist: "Riar Saab" },
  { title: "With You", artist: "AP Dhillon" },
  { title: "Excuses", artist: "AP Dhillon" },
  { title: "Brown Munde", artist: "AP Dhillon" },
  { title: "Tum Hi Ho", artist: "Arijit Singh" },
  { title: "Pasoori", artist: "Ali Sethi" },
  { title: "Maan Meri Jaan", artist: "King" },
  { title: "Tere Vaaste", artist: "Varun Jain" }
];

export default function App() {
  const [search, setSearch] = useState("");
  const [current, setCurrent] = useState(null);
  const [dark, setDark] = useState(true);

  const filteredSongs = songsData.filter(song =>
    song.title.toLowerCase().includes(search.toLowerCase()) ||
    song.artist.toLowerCase().includes(search.toLowerCase())
  );

  return (
    <div className={dark ? "app dark" : "app light"}>

      {/* Header */}
      <header>
        <h1>🎵 Foofliy</h1>
        <button onClick={() => setDark(!dark)}>
          {dark ? "☀️ Light" : "🌙 Dark"}
        </button>
      </header>

      {/* Search */}
      <input
        className="search"
        placeholder="Search Indian songs..."
        value={search}
        onChange={(e) => setSearch(e.target.value)}
      />

      {/* Song List */}
      <div className="glass">
        {filteredSongs.map((song, index) => (
          <div
            key={index}
            className="song"
            onClick={() => setCurrent(song)}
          >
            <strong>{song.title}</strong>
            <span>{song.artist}</span>
          </div>
        ))}
      </div>

      {/* Player */}
      {current && (
        <div className="player">
          Now Playing: <b>{current.title}</b> – {current.artist}
        </div>
      )}
    </div>
  );
}
