
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var clientContext = "d45324c1-fcb5-430a-902c-f20af696537c";

var duckOthers = False;

var level = 50;

var participant = "632899f8-2ea1-4604-8413-27bd2892079f";

var sourceLevels = new List<AudioSourceLevel>();
sourceLevels.Add(new AudioSourceLevel(participant,level,duckOthers));

var ducking = new AudioDuckingConfiguration
{
	RampActive = 50,
	RampInactive = 50,
	LowerLevel = 10,
	UpperLevel = 50,
};

var exclusive = True;

var participant = "550fae72-d251-43ec-868c-373732c2704f";

var participantMixerLevels = new List<ParticipantMixerLevel>();
participantMixerLevels.Add(new ParticipantMixerLevel(participant,exclusive,ducking,sourceLevels));

await graphClient.App.Calls["{id}"].Participants
	.ConfigureMixer(participantMixerLevels,clientContext)
	.Request()
	.PostAsync()

```