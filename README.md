# JS
# Download 1 file without view sorce on IE

    var anchor = document.createElement('a');
    anchor.href = result.url;
    anchor.target = '_blank';
    anchor.download = result.name;
    anchor.click();


# Timer seconds
    function timer() {
            $('.countdown').each(function() {
                var seconds = $(this).attr('data');
                $(this).attr('data',seconds-1);
                var id = $(this).attr('id');

                var days        = Math.floor(seconds/24/60/60);
                var hoursLeft   = Math.floor((seconds) - (days*86400));
                var hours       = Math.floor(hoursLeft/3600);
                var minutesLeft = Math.floor((hoursLeft) - (hours*3600));
                var minutes     = Math.floor(minutesLeft/60);
                var remainingSeconds = seconds % 60;
                if (remainingSeconds < 10) {
                    remainingSeconds = "0" + remainingSeconds;
                }
                $('.'+id).html(hours+(24*days) + ":" + minutes + ":" + remainingSeconds);
                if (seconds <= 0) {
                    //clearInterval(countdownTimer);
                    $('.'+id).html("Finished! ");
                } else {
                    seconds--;
                }
            });
        }
