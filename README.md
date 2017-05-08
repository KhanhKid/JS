# JS
# Download 1 file without view sorce on IE

    var anchor = document.createElement('a');
    anchor.href = result.url;
    anchor.target = '_blank';
    anchor.download = result.name;
    anchor.click();
