package me.devmuca.anunciar;

import org.bukkit.Bukkit;
import org.bukkit.command.Command;
import org.bukkit.command.CommandExecutor;
import org.bukkit.command.CommandSender;
import org.bukkit.entity.Player;

public class Commands implements CommandExecutor{

	@Override
	public boolean onCommand(CommandSender sender, Command cmd, String lb, String[] args) {
		
		if(cmd.getName().equalsIgnoreCase("anunciar"));
		 if (args.length == 0) {
		
		if(!(sender instanceof Player)) {
			
			sender.sendMessage("§cApenas jogadores podem executar este comando!");
			
		} else {
			
			if(!sender.hasPermission("mucanuncio.usar"));
			
			sender.sendMessage("&cVocê não tem permissão para executar este comando.");
			return true;
		}
		
    	Player p = (Player)sender;
        p.sendMessage("§7");
        p.sendMessage("§a                    [Anuncio]");
        p.sendMessage("§7");
        p.sendMessage("§fDigite §e/anunciar troca (Troca) §fPara anunciar uma troca");
        p.sendMessage("§fDigite §e/anunciar msg (Mensagem) §fPara anunciar uma mensagem");
        p.sendMessage("§7");
        
        if (args.length >= 1) {        
            StringBuilder sb = new StringBuilder();
            for (int i = 0; i < args.length; i++) 
                 sb.append(args[i]+" ");
      }
	       String sb = null;
	       
        	if (args [1] .equalsIgnoreCase ("msg")) { 
        	       Bukkit.broadcastMessage("§7");
        	       Bukkit.broadcastMessage("§a                   [Anuncio]");
        	       Bukkit.broadcastMessage("§7");
        	       Bukkit.broadcastMessage("§feO jogador §a" + p.getName() + "§eAnunciou");
				   Bukkit.broadcastMessage(sb);
        	       Bukkit.broadcastMessage("§f");
        	} 
        	}	
	
	
		return false;
	}

}
