stat
====

Personal fork of the stat effect in <a href = "http://sox.sourceforge.net/"> SOX</a>. Provides an additional option for JSON output. If you're tired of parsing the output of SOX and would rather use JSON, compile SOX with this version of stat.c. To use, just add a '-json' flag after you call stat, like this: 

```bash
$ sox somefile.wav -n stat -json
```
Output is standard, easy to use, JSON:
```bash
{
	"samplesRead" : 657090,
	"lengthInSeconds" : 14.900000,
	"scaledBy" : 2147483647.000000,
	"maximumAmplitude" : 0.434052,
	"minimumAmplitude" : -0.528595,
	"midlineAmplitude" : -0.047272,
	"meanNorm" : 0.044004,
	"meanAmplitude" : -0.000000,
	"RMSAmplitude" : 0.074119,
	"maximumDelta" : 0.171356,
	"minimumDelta" : 0.000000,
	"meanDelta" : 0.004453,
	"RMSDelta" : 0.009420,
	"roughFrequency" : 891,
	"volumeAdjustment" : 1.891808
}
```

