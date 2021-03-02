# binkdstat-vh-g
binkdstat - binkd statistic generator v1.21, (c)opyright by val khokhlov
            updated by Stas Degteff 2:5080/102@fidonet

    binkdstat [-l <log>] [-s <start>|- <period>|-] [-g <day>] [-b]
       -l <log>, --log=<log>                           use binkd.log <log>
       -s <start> <period>, --stat=<start>,<period>    set period for summary
       -g <day>, --graph=<day>                         set day to draw a graph
       -b                                              dispay failures table

    If <log> isn't specified, stdin is used
    Date/time consists of token(s): [+-]<NN>[hdwmy]
       use 15x to set value to 15 (h - hour, d - day, m - month, y - year)
       use +2d to advance day forward by 2, -6d to advance day backward by 6
       use -1w to set date to Monday of previous week, +1w - next week
       (if letter [hdwmy] is omitted 'd' is assumed)
    <start> and/or <period> can be '-' not to limit corresponding parameter
    <period> for --stat is relative to the <start> date/time (or current day)
    <day> for --graph is relative to the day after --stat (or current day)

    Examples:
       binkdstat -s -1w +7d            statistics for the previous week
       binkdstat -s -1 +1 -g -1        stats and graph for yesterday
