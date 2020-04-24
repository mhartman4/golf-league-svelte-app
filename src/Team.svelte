<script>
	export let team, placeNumber;
	let id = team.id.$t.replace("https://spreadsheets.google.com/feeds/list/1YsZn_ovmbxOE8gUlmAT7z_nUv5mg9qRdwnNAX-lIrnI/2/public/full/", "")
	let teamName = team.gsx$team.$t
	let owner = team.gsx$owner.$t
</script>


<div class="panel panel-default">
	<a class="click-track" data-toggle="collapse" href="collapse{id}">
		<div class="panel-heading">
			<table border="0" width="100%">
				<tbody>
					<tr>
						<td class="standings-place-number" width="30">{placeNumber}</td>
						<td width="75">
							<img class="player-photo" src="https://pga-tour-res.cloudinary.com/image/upload/c_fill,dpr_2.0,f_auto,g_face:center,h_125,q_auto,t_headshots_leaderboard_l,w_125/headshots_{team.roster[0].id}.png" width="45" height="45">
						</td>
						<td class="team-name">
							{teamName}<br>
							<span class="owner">{owner}</span>
						</td>
						<td class="team-earnings">
							{numeral(team.totalMoney).format('$0,0')}<br>
						</td>
					</tr>
				</tbody>
			</table>
		</div>
	</a>
</div>


<style>
	.panel {
    margin-bottom: 0;
    border-radius: 4px;
  }
	.standings-place-number {
    color: black;
    margin: 0px 5px;
    padding-left: 5px;
    font-size: 12px;
    text-align: left;
	}
	.player-photo {
    margin: 0px 8px;
 }
	.team-name {
    font-size: 16px;
    margin: 0px 8px;
    color: #46404A;
	}
	.owner {
    color: lightslategrey;
    font-size: 12px;
    font-family: "Roboto";
    margin-top: 10px;
	}
	.team-earnings {
    color: #46404A;
    font-size: 16px;
    padding: 0px 0px;
    text-align: right;
}
</style>