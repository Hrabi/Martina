# Aktivní claims agentů

Před souběžnou editací sem vlastník zkopíruje `workflow/templates/claim.md` pod názvem odpovídajícím ID tasku. Claim je provozní zámek nad `owned_paths`; před zahájením je nutné ověřit, že se nepřekrývají s jiným aktivním claimem.

Po převzetí handoffu claim odstraní koordinátor. Historie práce zůstává v tasku a Gitu; aktivní claimy se nepoužívají jako archiv.
