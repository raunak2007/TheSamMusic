<html>
<head>
    <title>Song Search</title>
    <style>
        table {
            border-collapse: collapse;
            width: 100%;
        }
        th, td {
            text-align: left;
            padding: 8px;
        }
        tr:nth-child(even) {
            background-color: teal;
            color: gold;
        }
        #searchInput {
            width: 100%;
            padding: 12px 20px;
            margin-bottom: 12px;
        }
    </style>
</head>
<body>
    <h1>Song Search</h1>

    <input type="text" id="searchInput" placeholder="Search for a song or artist...">
    
<table id="songTable">
    <tr>
        <th>Song</th>
        <th>Artist</th>
        <th>Duration</th>
        <th>Date</th>
    </tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8xg3vE8Ie_E">Love Story</a></td>
    <td>Taylor Swift</td>
    <td>3:56</td>
    <td>2008</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=th0cKJrFmFk">Circles</a></td>
    <td>Post Malone</td>
    <td>3:34</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=CevxZvSJLk8">Roar</a></td>
    <td>Katy Perry</td>
    <td>3:42</td>
    <td>2013</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=fRh_vgS2dFE">Sorry</a></td>
    <td>Justin Bieber</td>
    <td>3:20</td>
    <td>2015</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=75kTjG2ND3c">Drip Too Hard</a></td>
    <td>Lil Baby</td>
    <td>2:25</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=e-ORhEE9VVg">Blank Space</a></td>
    <td>Taylor Swift</td>
    <td>3:51</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=UceaB4D0jpo">Rockstar</a></td>
    <td>Post Malone</td>
    <td>3:38</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=QGJuMBdaqIw">Firework</a></td>
    <td>Katy Perry</td>
    <td>3:48</td>
    <td>2010</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8EJ3zbKTWQ8">Yummy</a></td>
    <td>Justin Bieber</td>
    <td>3:30</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=YnVISwXViSU">Woah</a></td>
    <td>Lil Baby</td>
    <td>3:03</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=nfWlot6h_JM">Shake It Off</a></td>
    <td>Taylor Swift</td>
    <td>3:39</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=QcIy9NiNbmo">Bad Blood</a></td>
    <td>Taylor Swift</td>
    <td>3:19</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=m7Bc3pLyij0">Happier</a></td>
    <td>Marshmello ft. Bastille</td>
    <td>3:34</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=OPf0YbXqDm0">Uptown Funk</a></td>
    <td>Mark Ronson ft. Bruno Mars</td>
    <td>4:30</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=BQ0mxQXmLsk">Havana</a></td>
    <td>Camila Cabello ft. Young Thug</td>
    <td>3:36</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=w2Ov5jzm3j8">Old Town Road</a></td>
    <td>Lil Nas X ft. Billy Ray Cyrus</td>
    <td>1:53</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=kJQP7kiw5Fk">Despacito</a></td>
    <td>Luis Fonsi ft. Daddy Yankee</td>
    <td>3:48</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=hLQl3WQQoQ0">Someone Like You</a></td>
    <td>Adele</td>
    <td>4:45</td>
    <td>2011</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=ru0K8uYEZWw">Can't Stop the Feeling!</a></td>
    <td>Justin Timberlake</td>
    <td>3:56</td>
    <td>2016</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8CdcCD5V-d8">Love Story (Taylor's Version)</a></td>
    <td>Taylor Swift</td>
    <td>4:06</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8xg3vE8Ie_E">You Belong with Me</a></td>
    <td>Taylor Swift</td>
    <td>3:51</td>
    <td>2008</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8Af372EQLck">Blank Space (Acoustic)</a></td>
    <td>Taylor Swift</td>
    <td>3:53</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=-CmadmM5cOk">Style</a></td>
    <td>Taylor Swift</td>
    <td>3:51</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=WsptdUFthWI">Delicate</a></td>
    <td>Taylor Swift</td>
    <td>3:52</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=IdneKLhsWOQ">Wildest Dreams</a></td>
    <td>Taylor Swift</td>
    <td>3:40</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=IhP3J0j9JmY">Believer</a></td>
    <td>Imagine Dragons</td>
    <td>3:23</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=uxpDa-c-4Mc">Hotline Bling</a></td>
    <td>Drake</td>
    <td>4:27</td>
    <td>2015</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=zABLecsR5UE">Someone You Loved</a></td>
    <td>Lewis Capaldi</td>
    <td>3:02</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=YrLk4vdY28Q">Hallelujah</a></td>
    <td>Leonard Cohen</td>
    <td>4:39</td>
    <td>1984</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=ktvTqknDobU">Radioactive</a></td>
    <td>Imagine Dragons</td>
    <td>3:08</td>
    <td>2012</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=rYEDA3JcQqw">Rolling in the Deep</a></td>
    <td>Adele</td>
    <td>3:49</td>
    <td>2010</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=eDdI7GhZSQA">Hey Jude</a></td>
    <td>The Beatles</td>
    <td>7:11</td>
    <td>1968</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=fJ9rUzIMcZQ">Bohemian Rhapsody</a></td>
    <td>Queen</td>
    <td>5:55</td>
    <td>1975</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=EqPtz5qN7HM">Hotel California</a></td>
    <td>The Eagles</td>
    <td>6:30</td>
    <td>1976</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=xpVfcZ0ZcFM">God's Plan</a></td>
    <td>Drake</td>
    <td>3:18</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=RIZdjT1472Y">One Dance</a></td>
    <td>Drake ft. WizKid & Kyla</td>
    <td>2:54</td>
    <td>2016</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=TcaOYnDd3FE">In My Feelings</a></td>
    <td>Drake</td>
    <td>3:38</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=EgBJmlPo8Xw">Hotline Bling</a></td>
    <td>Drake</td>
    <td>4:27</td>
    <td>2015</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=hpRvjBwVWZw">Controlla</a></td>
    <td>Drake</td>
    <td>4:05</td>
    <td>2016</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=LE6P8wq3l_4">Money In The Grave</a></td>
    <td>Drake ft. Rick Ross</td>
    <td>3:25</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=RubBzkZzpUA">Started From the Bottom</a></td>
    <td>Drake</td>
    <td>3:04</td>
    <td>2013</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=hb8VmnsH4X4">Nonstop</a></td>
    <td>Drake</td>
    <td>3:58</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=COpc1eZaabk">Passionfruit</a></td>
    <td>Drake</td>
    <td>4:58</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=cimoNqiulUE">Headlines</a></td>
    <td>Drake</td>
    <td>3:56</td>
    <td>2011</td>
</tr>

<tr>
    <td><a href="https://www.youtube.com/watch?v=0VR3dfZf9Yg">Emotionally Scarred</a></td>
    <td>Lil Baby</td>
    <td>3:17</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=WoF7DzQwKBE">Woah</a></td>
    <td>Lil Baby</td>
    <td>3:03</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=kcF4X7Jj9XQ">The Bigger Picture</a></td>
    <td>Lil Baby</td>
    <td>4:10</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=DkKPBToZVBw">On Me</a></td>
    <td>Lil Baby</td>
    <td>2:32</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8pFvdG0wEM0">Sum 2 Prove</a></td>
    <td>Lil Baby</td>
    <td>3:23</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=KFDr2S6fEjc">We Paid</a></td>
    <td>Lil Baby ft. 42 Dugg</td>
    <td>2:50</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=0JMlW2paZnU">Close Friends</a></td>
    <td>Lil Baby</td>
    <td>3:23</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=xN8or7VrZ1o">Freestyle</a></td>
    <td>Lil Baby</td>
    <td>2:43</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=v2AC41dglnM">Yes Indeed</a></td>
    <td>Lil Baby ft. Drake</td>
    <td>2:22</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8j4CEfEw3_o">All In</a></td>
    <td>Lil Baby</td>
    <td>2:38</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=ZmDBbnmKpqQ">Drivers License</a></td>
    <td>Olivia Rodrigo</td>
    <td>4:02</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8ZnU7aF0T0E">Deja Vu</a></td>
    <td>Olivia Rodrigo</td>
    <td>3:36</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=gNi_6U5Pm_o">Good 4 U</a></td>
    <td>Olivia Rodrigo</td>
    <td>2:58</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=W0LdEg2Sd3M">Brutal</a></td>
    <td>Olivia Rodrigo</td>
    <td>2:23</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=xJXJbD0OSg4">Traitor</a></td>
    <td>Olivia Rodrigo</td>
    <td>3:49</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=Q22DITf6w3s">Favorite Crime</a></td>
    <td>Olivia Rodrigo</td>
    <td>2:33</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=qiuNr0E4Wgk">Happier</a></td>
    <td>Olivia Rodrigo</td>
    <td>4:16</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=0Bf3CqbeSDU">Jealousy, Jealousy</a></td>
    <td>Olivia Rodrigo</td>
    <td>3:34</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=5OnTbL4oMWI">Enough for You</a></td>
    <td>Olivia Rodrigo</td>
    <td>3:20</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=sO0zljgSX2w">Hope Ur OK</a></td>
    <td>Olivia Rodrigo</td>
    <td>3:14</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=JGwWNGJdvx8">Shape of You</a></td>
    <td>Ed Sheeran</td>
    <td>3:53</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=LPnNUfvb6WY">Thinking Out Loud</a></td>
    <td>Ed Sheeran</td>
    <td>4:41</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=9Gt__LQo7Xk">Photograph</a></td>
    <td>Ed Sheeran</td>
    <td>4:35</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=t4Y1lUfH7Ig">Perfect</a></td>
    <td>Ed Sheeran</td>
    <td>4:23</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=ABhDiXbUaBE">Castle on the Hill</a></td>
    <td>Ed Sheeran</td>
    <td>4:21</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=eiDiKwbGfIY">The A Team</a></td>
    <td>Ed Sheeran</td>
    <td>4:50</td>
    <td>2011</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=3tmd-ClpJxA">Galway Girl</a></td>
    <td>Ed Sheeran</td>
    <td>2:50</td>
    <td>2017</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=Z1oN7O-4p_8">I Don't Care</a></td>
    <td>Ed Sheeran & Justin Bieber</td>
    <td>3:41</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=DYRg2AqzVjI">Don't</a></td>
    <td>Ed Sheeran</td>
    <td>3:39</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=l9DhEX6RUW8">Bloodstream</a></td>
    <td>Ed Sheeran</td>
    <td>5:00</td>
    <td>2014</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=Jg5wkZ-dJXA">Stronger</a></td>
    <td>Kanye West</td>
    <td>5:12</td>
    <td>2007</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=1N3JUSJz8oA">Heartless</a></td>
    <td>Kanye West</td>
    <td>3:31</td>
    <td>2008</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=PAt2m3V-GHQ">Gold Digger</a></td>
    <td>Kanye West ft. Jamie Foxx</td>
    <td>3:42</td>
    <td>2005</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=HAfFfqiYLp0">Jesus Walks</a></td>
    <td>Kanye West</td>
    <td>3:13</td>
    <td>2004</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=6vwNcNOTVzY">Stronger (Live from The Joint)</a></td>
    <td>Kanye West</td>
    <td>3:25</td>
    <td>2008</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=6CHs4x2uqcQ">All of the Lights</a></td>
    <td>Kanye West ft. Rihanna, Kid Cudi</td>
    <td>5:00</td>
    <td>2010</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=QGJuMBdaqIw">Stronger (Graduation)</a></td>
    <td>Kanye West</td>
    <td>5:12</td>
    <td>2007</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=4B_UYYPb-Gk">Can't Tell Me Nothing</a></td>
    <td>Kanye West</td>
    <td>4:32</td>
    <td>2007</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=p_RqWocthcc">Famous</a></td>
    <td>Kanye West</td>
    <td>3:16</td>
    <td>2016</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=ohH2brF6-Uk">Black Skinhead</a></td>
    <td>Kanye West</td>
    <td>3:08</td>
    <td>2013</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=X6foS0VtIOc">Bound 2</a></td>
    <td>Kanye West</td>
    <td>3:50</td>
    <td>2013</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8kyWDhB_QeI">Waves</a></td>
    <td>Kanye West ft. Chris Brown</td>
    <td>3:01</td>
    <td>2016</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=Bm5iA4Zupek">Flashing Lights</a></td>
    <td>Kanye West ft. Dwele</td>
    <td>3:58</td>
    <td>2007</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=7vCImzUzMw4">Touch the Sky</a></td>
    <td>Kanye West ft. Lupe Fiasco</td>
    <td>3:57</td>
    <td>2006</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=kJv5D0Ca3G0">Ultralight Beam</a></td>
    <td>Kanye West ft. Chance the Rapper</td>
    <td>5:20</td>
    <td>2016</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=_xk8UMIvKwU">Follow God</a></td>
    <td>Kanye West</td>
    <td>1:44</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=6RcqkP6n4hY">Closed on Sunday</a></td>
    <td>Kanye West</td>
    <td>2:34</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=LQ488QrqGE4">On God</a></td>
    <td>Kanye West</td>
    <td>2:36</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=AgAQjsX02fM">Wash Us in the Blood</a></td>
    <td>Kanye West ft. Travis Scott</td>
    <td>3:10</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=Pyazlxm02vI">God Is</a></td>
    <td>Kanye West</td>
    <td>3:24</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=8kyWDhB_QeI">All Falls Down</a></td>
    <td>Kanye West ft. Syleena Johnson</td>
    <td>3:43</td>
    <td>2004</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=p3L2uACuC9A">Graduation</a></td>
    <td>Kanye West</td>
    <td>1:23</td>
    <td>2007</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=H5EvvswsNtI">Homecoming</a></td>
    <td>Kanye West ft. Chris Martin</td>
    <td>3:23</td>
    <td>2007</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=VDj9QIhU1DY">Ransom</a></td>
    <td>Lil Tecca</td>
    <td>2:11</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=BCxnmd9zpw4">Love Me</a></td>
    <td>Lil Tecca</td>
    <td>2:06</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=iXYpYH0JFfw">Did It Again</a></td>
    <td>Lil Tecca</td>
    <td>2:18</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Molly Girl</a></td>
    <td>Lil Tecca</td>
    <td>1:58</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=DmMp-LSc4SM">Bossanova</a></td>
    <td>Lil Tecca</td>
    <td>2:15</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=hxwePvdHZeI">Out of Love</a></td>
    <td>Lil Tecca</td>
    <td>1:55</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=rLlU1gwF74E">Dolly</a></td>
    <td>Lil Tecca</td>
    <td>2:19</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=lG8fWx982Qs">Count Me Out</a></td>
    <td>Lil Tecca</td>
    <td>2:32</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=ImFP_U_YlR0">Sidenote</a></td>
    <td>Lil Tecca</td>
    <td>1:49</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=dgIxrAdFkeE">Shots</a></td>
    <td>Lil Tecca</td>
    <td>2:23</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=_P8S6l3cl3g">Royal Rumble</a></td>
    <td>Lil Tecca</td>
    <td>1:57</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=eIrCLI0p-2M">Weatherman</a></td>
    <td>Lil Tecca</td>
    <td>2:29</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=IFiVsR8cY9w">Our Time</a></td>
    <td>Lil Tecca</td>
    <td>2:18</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=zr_zvON_E9E">Love No Thotties</a></td>
    <td>Lil Tecca</td>
    <td>2:10</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=IOyM7Hv4vRo">No Answers</a></td>
    <td>Lil Tecca</td>
    <td>2:11</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=yTdXNGVo-g8">Somebody</a></td>
    <td>Lil Tecca</td>
    <td>2:21</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=dvFLxH3MMTA">Did It Again</a></td>
    <td>Lil Tecca</td>
    <td>2:33</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=Avptx2H2StI">Insecurities</a></td>
    <td>Lil Tecca</td>
    <td>2:18</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=52I0cK3iVVA">Closest to Heaven</a></td>
    <td>Lil Tecca</td>
    <td>2:25</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=1QFToqoFeLs">Seaside</a></td>
    <td>Lil Tecca</td>
    <td>1:46</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=1aQYBn6fgh4">ORANGE SODA</a></td>
    <td>Baby Keem</td>
    <td>3:01</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=qKpBd2k0Zak">no sense</a></td>
    <td>Baby Keem</td>
    <td>2:10</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=9jlsR-5KScQ">hooligan</a></td>
    <td>Baby Keem</td>
    <td>1:36</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=5RUwNMFdx04">FRANCE FREESTYLE</a></td>
    <td>Baby Keem</td>
    <td>2:21</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=_QJEGG2grX4">Buss Her Up</a></td>
    <td>Baby Keem</td>
    <td>1:52</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=I4AvWxKwNwU">auntie</a></td>
    <td>Baby Keem</td>
    <td>2:14</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=i1GmxMTwUgs">stats</a></td>
    <td>Baby Keem</td>
    <td>2:35</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=yf9OAFML_EI">rookie of the year</a></td>
    <td>Baby Keem</td>
    <td>1:45</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=1FGrD0OHXJY">PUNK MUNK</a></td>
    <td>Baby Keem</td>
    <td>2:32</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=PXUSP9DZ9NU">pockets too big</a></td>
    <td>Baby Keem</td>
    <td>1:58</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=NEpXGvEe5Ow">honest</a></td>
    <td>Baby Keem</td>
    <td>1:57</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=WvfP-m4fyvM">Bully Beef</a></td>
    <td>Baby Keem</td>
    <td>2:04</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=QL6F3kgWKT4">Cocoa</a></td>
    <td>Baby Keem</td>
    <td>1:55</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=LdY_xGZjyHo">Rockstar P</a></td>
    <td>Baby Keem</td>
    <td>2:28</td>
    <td>2018</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=FDfIg8VC2vc">Let's Go Outside</a></td>
    <td>Baby Keem</td>
    <td>2:04</td>
    <td>2020</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=X3bzZVf1zXU">not my bro</a></td>
    <td>Baby Keem</td>
    <td>2:35</td>
    <td>2019</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=dXkUMZPLWwE">DURAG ACTIVITY</a></td>
    <td>Baby Keem ft. Travis Scott</td>
    <td>2:13</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=gnaAxLm_aIQ">Family Ties</a></td>
    <td>Baby Keem ft. Kendrick Lamar</td>
    <td>3:39</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=9EwR5QWCpy4">Trademark USA</a></td>
    <td>Baby Keem</td>
    <td>2:24</td>
    <td>2021</td>
</tr>
<tr>
    <td><a href="https://www.youtube.com/watch?v=XicK5zQYiXo">scapegoats</a></td>
    <td>Baby Keem</td>
    <td>1:56</td>
    <td>2021</td>
</tr>

</table>

    <script>
        const searchInput = document.getElementById('searchInput');
        const table = document.getElementById('songTable');
        const rows = table.getElementsByTagName('tr');
        
        searchInput.addEventListener('keyup', function() {
            const searchTerm = searchInput.value.toLowerCase();
            
            for (let i = 1; i < rows.length; i++) {
                const song = rows[i].getElementsByTagName('td')[0].textContent.toLowerCase();
                const artist = rows[i].getElementsByTagName('td')[1].textContent.toLowerCase();
                
                if (song.includes(searchTerm) || artist.includes(searchTerm)) {
                    rows[i].style.display = '';
                } else {
                    rows[i].style.display = 'none';
                }
            }
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html>
<head>
  <title>Music Playlist</title>
  <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
  <h1>My Music Playlist</h1>
  <input id="songInput" type="text" placeholder="Enter a song">
  <button id="addButton">Add Song</button>
  <ul id="playlist"></ul>

  <script>
    const playlist = document.getElementById('playlist');
    const songInput = document.getElementById('songInput');
    const addButton = document.getElementById('addButton');

    // Fetch the playlist from the backend and display it
    function fetchPlaylist() {
      fetch('/playlist')
        .then(response => response.json())
        .then(data => {
          playlist.innerHTML = '';
          data.forEach(song => {
            const li = document.createElement('li');
            li.innerHTML = song;
            playlist.appendChild(li);
          });
        });
    }

    // Add a song to the playlist
    function addSong() {
      const song = songInput.value;
      fetch('/playlist', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ song })
      })
      .then(fetchPlaylist);
    }

    // Attach event listeners
    addButton.addEventListener('click', addSong);

    // Initial fetch to display the playlist
    fetchPlaylist();
  </script>
</body>
</html>
