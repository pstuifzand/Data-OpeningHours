# NAME

Data::OpeningHours - Is a shop is open or closed at this moment?

# SYNOPSYS

    use DateTime;
    use Data::OpeningHours 'is_open';
    use Data::OpeningHours::Calendar;

    my $cal = Data::OpeningHours::Calendar->new();
    $cal->set_week_day(1, [['13:00','18:00']]); # monday
    $cal->set_week_day(2, [['09:00','18:00']]);
    $cal->set_week_day(3, [['09:00','18:00']]);
    $cal->set_week_day(4, [['09:00','18:00']]);
    $cal->set_week_day(5, [['09:00','21:00']]);
    $cal->set_week_day(6, [['09:00','17:00']]);
    $cal->set_week_day(7, []);
    $cal->set_special_day('2012-01-01', []);
    is_open($cal, DateTime->now());

# DESCRIPTION

Data::OpeningHours helps you create a widget that shows when a shop is open or
closed.

# AUTHOR

Peter Stuifzand <peter@stuifzand.eu>

# COPYRIGHT

Copyright 2013 - Peter Stuifzand

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

