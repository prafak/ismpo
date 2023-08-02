$(function () {
    if (window.rcmail) {
        rcmail.addEventListener('init', function (evt) {
            if (rcmail.task === 'settings') {

                // identities check focus && error class to input
                if (rcmail.env.action === 'edit-identity' || rcmail.env.action === 'add-identity') {
                    identityErrorDisplay();
                } else if (rcmail.env.action === 'plugin.managesieve-action') {
                    filtersRedirectInfo();
                } else if (rcmail.env.action === 'plugin.managesieve-vacation') {
                    vacationRedirectInfo();
                    vacationNewlineInfo()
                }
            }
        });
    }
});

var vacationRedirectInfo = function () {
    // info next to vacation save button

    var info = '<span class="ui-icon ui-icon-info" style="display: inline-block;"></span>'
        + rcmail.gettext('vacation_redirect_info', 'zoner_settings');

    $(".footerleft").append(info);
};

var vacationNewlineInfo = function () {
    var html = '<div style="opacity: 0.7;">' + rcmail.gettext('vacation_newline_info', 'zoner_settings') + '</div>'
    $('#vacation_addresses_list').next().after(html);
};

var filtersRedirectInfo = function () {
    // info next to filter save button

    var info = '<span class="ui-icon ui-icon-info" style="display: inline-block;"></span>'
        + rcmail.gettext('filter_redirect_info', 'zoner_settings');

    $("#footer .footerleft").append(info);
};


var identityErrorDisplay = function () {
    var $identity_mail = $("#rcmfd_email");

    if (rcmail.env.zs_identity_error) {
        $identity_mail
            .addClass('error')
            .focus();
    } else {
        $identity_mail
            .removeClass('error');
    }
};



