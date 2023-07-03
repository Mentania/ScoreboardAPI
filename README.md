# ScoreboardAPI

Einfach alle drei Klasse in eueren src einbinden

Nutzen tut ihr die Api dann wie Folgt:

public static void loadScoreboard(Player player) {

		ScoreboardAPI board = new ScoreboardAPI(player);

		board.updateTitle(ChatColor.GOLD + (String) config.get("Scoreboard.Header"));
		board.updateLines(

				"",  //Leer Zeile
				"§6Server",
				(String) config.get("Scoreboard.Server"),
				"",
				"&6Name",
				player.getDisplayName(),
				"",
				"§6Online",
				"§d§l" + Bukkit.getOnlinePlayers().size() + "§b§l/§c§l" + Bukkit.getMaxPlayers(),
				"",
				"§6Kontostand",
				"§d§l" + plugin.econ.format(plugin.econ.getBalance(player.getName())),
				""

				);

	}

 Die Config ist einfach bei mir im Plugin hinterlegt könnt dafür aber ganz einfach das eintragen was ihr wollt!
