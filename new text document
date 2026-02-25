SELECT *
FROM spotify_data_clean
WHERE explicit = 1;

SELECT *
FROM spotify_data_clean
WHERE track_popularity > 50;

SELECT DISTINCT artist_name
FROM spotify_data_clean;

SELECT album_name, COUNT(*) AS total_tracks
FROM spotify_data_clean
GROUP BY album_name;

SELECT album_id, album_name,
       AVG(track_duration_min) AS avg_track_duration
FROM spotify_data_clean
GROUP BY album_id, album_name;

SELECT track_name, artist_name, track_popularity
FROM spotify_data_clean
WHERE track_popularity = (
    SELECT MAX(track_popularity)
    FROM spotify_data_clean
);

SELECT artist_name, COUNT(*) AS total_tracks
FROM spotify_data_clean
GROUP BY artist_name
HAVING COUNT(*) > 1
ORDER BY total_tracks DESC;

SELECT album_id, album_name,
       AVG(track_popularity) AS avg_track_popularity
FROM spotify_data_clean
GROUP BY album_id, album_name
HAVING AVG(track_popularity) > 30
ORDER BY avg_track_popularity DESC;

SELECT artist_name,
       MAX(artist_followers) AS followers
FROM spotify_data_clean
GROUP BY artist_name
ORDER BY followers DESC
LIMIT 5;

SELECT album_release_date,
       COUNT(*) AS tracks_released
FROM spotify_data_clean
GROUP BY album_release_date
ORDER BY album_release_date;

SELECT album_release_date,
       COUNT(*) AS tracks_released
FROM spotify_data_clean
GROUP BY album_release_date
ORDER BY album_release_date;

SELECT *
FROM tracks
WHERE release_date > '2025-10-25';

SELECT *
FROM artists
WHERE genre IS NULL OR genre = '';
SELECT artist_name,
       AVG(track_popularity) AS avg_popularity
FROM tracks
GROUP BY artist_name
ORDER BY avg_popularity DESC
LIMIT 1;
