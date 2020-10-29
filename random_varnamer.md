random\_varnamer\_function
================
kanazian
10/25/2020

## Suggest some fun/temp variable names when you are stuck

### …because life is hard sometimes

Inspired by
<https://github.com/tomaztk/Useless_R_functions/blob/main/RJobTitleGenerator.R>
Thanks to shelby for having fun coming up with words User assumes all
responsibility for terrible code due to randomly named variables

``` r
library(tools)
Random_name <- function(n_out = 5, out = "snakecase") {
  adj <- unique(c("addicted","adorable","adventurous","aggressive","agreeable","alert","alive","amused","angry","annoyed","annoying","anxious","arrogant","ashamed","attractive","average","awful","bad","beautiful","better","bewildered","black","blended","bloody","blushing","bored","brainy","brave","breakable","bright","bright","busy","calm","careful","cautious","charming","cheerful","clean","clear","clever","cloudy","clumsy","colorful","combative","comfortable","concerned","condemned","confused","cooperative","courageous","crabby","crazy","creepy","crowded","cruel","curious","cute","dangerous","dark","dead","defeated","defiant","delightful","depressed","determined","different","difficult","disgusted","distinct","disturbed","dizzy","doubtful","drab","drab","dull","eager","easy","egregious","elated","elegant","embarrassed","enchanting","encouraging","energetic","enthusiastic","envious","evil","excited","expensive","exuberant","fair","faithful","famous","fancy","fantastic","fierce","filthy","fine","foolish","fragile","frail","frantic","friendly","frightened","funky","funny","gentle","gifted","glamorous","gleaming","glorious","good","gorgeous","graceful","gregarious","grieving","grotesque","grumpy","handsome","happy","healthy","helpful","helpless","hilarious","homeless","homely","horrible","humble","hungry","hurt","icky","ill","important","impossible","inexpensive","innocent","inquisitive","itchy","jealous","jellied","jittery","jolly","joyous","keratinous","kind","lazy","light","lively","lonely","long","lovely","lucky","lusty","magnificent","misty","modern","monotonous","motionless","muddy","mushy","mysterious","nasty","naughty","nervous","nice","noble","nutty","obedient","obnoxious","odd","ombre","oozy","open","outrageous","outstanding","panicky","perfect","petite","plain","pleasant","poised","poor","powerful","precious","prickly","proud","putrid","puzzled","quaint","quizzical","ragged","real","relieved","repulsive","rich","scary","selfish","sheepish","shiny","shy","silly","sleepy","smiling","smoggy","sore","sparkling","splendid","spotless","stormy","strange","stupid","successful","super","talented","tame","tasty","tender","tense","tepid","terrible","thankful","thoughtful","thoughtless","tired","tough","troubled","ugliest","ugly","uninterested","unsightly","unusual","upgraded","upset","uptight","vain","vast","victorious","vivacious","wandering","waxy","weak","weary","wicked","wild","witty","worried","worrisome","wrong","zany","zealous","zesty","zippy"))
  mod <- unique(c("acrid","airy","aqua","aquamarine","azure","baby","beefy","beige","big","bird","bisque","black","bland","blast","blue","bony","boundless","brackish","brass","brawny","brick","broad","bronze","brown","brulee","buff","bulbous","bulky","burly","butter","camel","caravan","cerulean","chalice","chartruse","chocolate","chowder","chunky","clove","colossal","compact","copper","coral","cornsilk","corny","corpulent","cosmic","cricket","crimson","crusty","cubby","curvy","cyan","dairy","dance","delight","dreaming","drops","dust","dwarf","eggy","elfin","emaciated","endless","enormous","enormous","epic","expansive","extensive","fat","feldspar","ferocious","fest","flash","fleshy","forlorn","fuchsia","galaxy","gargantuan","garish","garnished","gaunt","giant","gigantic","ginger","glorious","glow","gold","grain","grand","grass","gray","great","green","haggard","hangry","haphazard","heavy","hefty","hollow","honeydew","hue","huge","hulking","illimitable","immeasurable","immense","indigo","infinitesimal","inglorious","inky","ivory","julienned","jumbled","khaki","lanky","large","lavender","lean","light","lily","limber","lime","limitless","limp","linen","little","magenta","mammoth","mane","maroon","massive","meager","measly","microscopic","mini","miniature","minuscule","minute","moccasin","monstrous","moss","moth","mustard","narrow","navy","notorious","obese","olive","orange","orchid","outsized","oval","oversize","overweight","ovoid","palacial","pale","paltry","passion","pearl","pentagonal","peruvian","petite","pink","plateau","plum","plump","pollen","portly","poundcake","pudgy","puny","purple","quaint","quick","quiet","rabbit","rabid","red","ridge","rock","rotund","round","salmon","sand","scanty","scraggy","scrawny","sea","seed","shadow","short","sienna","silk","silver","sizable","skeletal","skimpy","skinny","slender","slim","small","snow","sorbet","souffle","split","spout","square","squat","stage","star","stocky","stone","stout","strapping","stupendous","sturdy","sunlight","swole","tail","tall","tan","tangerine","tart","tea","teal","teensy","teeny","terrible","thick","thickset","thin","thistle","tiny","titanic","tomato","towering","traditional","trifling","trim","tubby","turquoise","tweed","undersized","underweight","undulating","unlimited","vast","victorious","violet","vivacious","wee","wheat","white","whopping","wide","wild","wilted","withered","woods","xrayed","yellow","young","zesty"))
  #for some reason, c() for all obj names does not work, need to split into 2 vectors and then join vectors
  obj1 <- c("aardvark","ability","activity","addition","administration","advertising","advice","agency","agonist","alcohol","alligator","alp","alpaca","analysis","angle","antagonist","anteater","antelope","apartment","ape","apex","application","arabian","arbiter","arch","area","ariola","armadillo","army","art","arthropod","article","aspect","association","attention","attitude","audience","axe","axon","aye","babadook","baboon","badger","band","bandicoot","bangalore","bank","banshee","baratheons","basidia","basis","bat","bear","beaver","belly","beluga","bicycle","bird","bison","blood","bloodhound","boar","bobcat","bonobo","bork","boyfriend","brake","bridge","brute","bud","buffalo","bug","bulb","bull","bunker","burger","cacophony","caiman","camel","camera","cannon","canoe","capuchin","capybara","carbine","caribou","cassette","cat","category","cattle","cell","centromere","chain","chainsaw","cheetah","chemistry","child","chimpanzee","chinchilla","chipmunk","cigarette","cilia","city","clathrin","climax","cobra","cocktail","cog","collection","college","combination","community","competition","computer","concept","connection","context","control","coral","cortana","cougar","country","county","covenant","cow","coyote","cozies","crankset","crispr","criticism","crocodile","croissant","crustacean","cucumber","cumquat","curb","customer","dartfrog","data","dealer","death","debt","decision","deer","definition","degus","dendrite","department","depression","depth","description","development","difference","dikdik","dingo","direction","director","direwolf","discussion","disease","disk","distribution","dogfish","dolphin","donkey","doodle","dormouse","dragon","driver","drone","drunkard","duckbill","dugong","economics","education","effort","eggplant","elephant","elevation","elite","elk","endoplasmic_reticulum","energy","enoki","entertainment","environment","epic","equipment","ermine","estate","eunuch","event","exam","exon","expression","fact","failure","fairy","family","ferret","finding","fish","fishing","flash","flight","flood","flop","food","foundation","fox","freedom","frog","gateway","gazelle","gear","gecko","gel","ghost","gibbon","giraffe","glomerulus","glove","goal","goalie","goat","goat","golgi","gopher","gorilla","government","grandmother","grandpa","gravemind","greyjoy","greyworm","grizzly","groundhog","grove","growth","grunt","guineapig","gulag","gulash","gutter","halibut","halo","hammerheadshark","hare","health","heart","hedgehog","helmet","heretic","hippo","hiseq","histone","history","hockey","hornet","horse","horse","housing","humpback","hunter","hyena","hyrax","idea","igloo","iguana","iguana","imagination","impala","importance","income","incubator","industry","inflation","information","insect","instance","insurance","internet","introduction","intron","investment","irrawaddy","jackal","jackrabbit","jaguar","jellyfish","johnson","jumprope","jungle","kangaroo","keyes","khal","khaleesi","killerwhale","kingsguard","kingslayer","klondike","knowledge","koala","komodo","kookaburra","kryll","ladder","lake","lama","lamb","lance","lancelet","lane","language","lannisters","law","leatherback","lemming","lemur","length","leopard","library","ligand","linda","lion","lipid","literature","llama","location","locust","loggerhead","loris","love","lynx")
  obj2 <- c("magazine","magnet","mako","mama","management","manatee","mantaray","mantis","map","marketing","marmot","marriage","martells","math","meaning","meat","media","medicine","meerkat","member","membrane","memory","mercenary","message","method","minion","mink","miseq","mitochondria","mole","mollusk","moment","mongoose","mongoose","monkey","monkey","month","mood","moose","mouse","movie","mule","music","muskox","muskrat","myelin","nakedmolerat","narwhal","nation","nature","nautilus","nessie","neuron","news","newspaper","newt","nextseq","nexus","night","nipple","nucleus","nutria","nyala","ocelot","octane","octopus","odorant","office","okapi","opinion","opossum","opportunity","orangutan","orca","organelle","organization","otter","outback","oven","ox","painting","panda","pangolin","panther","paper","passion","paw","payment","pbody","pedal","people","percentage","performance","person","personality","perspective","philosophy","phone","photo","photon","physics","pig","pilot","pinemarten","pinky","pipette","pistol","pizza","platypus","player","poisson","polarbear","policy","politics","population","porcupine","pore","porpoise","possum","potto","power","prairiedog","president","problem","product","property","prophet","psychology","pudu","puma","puma","pylon","quality","quint","quokkas","quolls","quorum","rabbit","raccoon","radio","ramen","rat","ray","reading","reality","receptor","recipe","recommendation","regret","reindeer","relationship","resource","response","responsibility","revolver","rhino","road","role","rollercoaster","safety","salamander","sandsnakes","sanguine","scarab","scene","science","scorpion","seal","seat","secretary","security","selection","sept","sequoia","series","setting","shakeweight","shark","sheath","sheep","sheep","shifter","shiitake","shopping","shotgun","situation","skill","skin","skink","skunk","sloth","smg","snake","sniper","snowleopard","society","software","solution","soup","spartan","spatula","spectre","spermwhale","spidermonkey","spore","squirrel","squirrel","starks","statement","stirbar","storage","story","stranger","strategy","stripper","student","studio","success","sufferfest","sunbear","swarm","system","takin","tamarin","tapir","tardigrade","targaryens","tasmaniandevil","tattoo","teacher","teaching","technology","television","telomere","temperature","terrapin","theory","thing","thought","tiger","titan","topi","topic","tortoise","tower","transposon","trojan","troll","trombone","truth","truth","tuba","tube","tullys","turtle","uakari","understanding","unibrow","unicorn","unit","university","unsullied","user","vampirebat","variety","veldt","version","vesicle","vicuna","video","vixen","volcano","vole","vuvuzela","wall","wallaby","walrus","wangjangler","warthog","warthog","waterbuffalo","watt","way","wealth","weasel","week","whale","whisk","wildcat","wildebeest","wildfire","witch","wobbegong","wolf","wolverine","woman","wombat","wood","woodchuck","world","wraith","wretches","writing","xenon","yak","year","yeast","yule","zamboni","zebra","zebu","zion","zulu")
  obj <- unique(c(obj1, obj2))
  
  #less likely to make 3 word names
  add_mod <- as.logical(round(runif(round(n_out), min = 0, max = 0.85)))
  name_vec <- vector(mode = "character", length = n_out)
  
  for (i in 1:round(n_out)) {
    #return 3 word names
    if (add_mod[i] == TRUE) {
      #handle output as snake or camelcase
      if (stringr::str_detect(out, "camel")) {
        name_vec[i] <- paste(toTitleCase(sample(adj, 1)), 
                             toTitleCase(sample(mod, 1)), 
                             toTitleCase(sample(obj, 1)), 
                             sep = "")
      } else {
        name_vec[i] <- paste(sample(adj, 1), 
                             sample(mod, 1), 
                             sample(obj, 1), sep = "_")
      } #endif
      #return 2 word names
    } else {
      if (stringr::str_detect(out, "camel")) {
        name_vec[i] <- paste(ifelse(as.logical(round(runif(1))), 
                                    toTitleCase(sample(adj, 1)), 
                                    toTitleCase(sample(mod, 1))),
                                    toTitleCase(sample(obj, 1)), sep = "")
      } else {
        name_vec[i] <- paste(ifelse(as.logical(round(runif(1))), 
                                    sample(adj, 1), 
                                    sample(mod, 1)),
                                    sample(obj, 1), sep = "_")
      } #endif 
    } #endif
  } #endfor
  return(name_vec)
} #endfunc

Random_name(10)
```

    ##  [1] "handsome_lipid"            "spotless_pale_oven"       
    ##  [3] "curious_watt"              "blushing_cosmic_education"
    ##  [5] "fest_advice"               "giant_muskox"             
    ##  [7] "nasty_bangalore"           "joyous_bird_tube"         
    ##  [9] "clumsy_population"         "bewildered_television"

``` r
Random_name(3, out = "camelcase")
```

    ## [1] "PlumpBloodhound" "RockGoal"        "CrowdedFrog"
