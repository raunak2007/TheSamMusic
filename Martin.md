<Script>
def sort_music(music_list):
    return sorted(music_list, key=lambda track: track['duration'])
music_list = [
    {'title': 'Song1', 'artist': 'Artist1', 'duration': 200},
    {'title': 'Song2', 'artist': 'Artist2', 'duration': 150},
    {'title': 'Song3', 'artist': 'Artist3', 'duration': 180},
]
sorted_music = sort_music(music_list)
for track in sorted_music:
    print(f"Title: {track['title']}, Artist: {track['artist']}, Duration: {track['duration']}")
3:04
def filter_artist(music_list, artist_name):
    return [track for track in music_list if track['artist'].lower() == artist_name.lower()]
def sort_music(music_list):
    return sorted(music_list, key=lambda track: track['duration'])
music_list = [
    {'title': 'Song1', 'artist': 'Artist1', 'duration': 200},
    {'title': 'Song2', 'artist': 'Artist2', 'duration': 150},
    {'title': 'Rockstar', 'artist': 'Post Malone', 'duration': 218},
    {'title': 'Circles', 'artist': 'Post Malone', 'duration': 215},
    {'title': 'Congratulations', 'artist': 'Post Malone', 'duration': 223},
    {'title': 'Song3', 'artist': 'Artist3', 'duration': 180},
]
post_malone_tracks = filter_artist(music_list, 'Post Malone')
sorted_music = sort_music(post_malone_tracks)
for track in sorted_music:
    print(f"Title: {track['title']}, Artist: {track['artist']}, Duration: {track['duration']}")
</script>