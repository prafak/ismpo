($(function () {
    // disable dark mode on login page. Also see zoner_login.css
    $('html').removeClass('dark-mode');

    $showPassBtn = $('<div id="show-pass" title="' + rcmail.gettext('show_pass', 'zoner_login') + '"><span class="show"></span></div>');
    $icon = $showPassBtn.find('span');
    $loginInput = $('#rcmloginpwd');

    $showPassBtn.on('click', function () {
        if ($loginInput.attr('type') === 'password') {
            $loginInput.attr('type', 'text');
            $icon.addClass('hide');
            $showPassBtn.attr('title', rcmail.gettext('hide_pass', 'zoner_login'));
        } else {
            $loginInput.attr('type', 'password');
            $icon.removeClass('hide');
            $showPassBtn.attr('title', rcmail.gettext('show_pass', 'zoner_login'));
        }
    });

    $('#rcmloginpwd').before($showPassBtn);
}));