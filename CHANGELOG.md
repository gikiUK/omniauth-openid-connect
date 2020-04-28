
# v0.3.3 (09.11.2019)

- Pass `acr_values` to authorize url [#43](https://github.com/m0n9oose/omniauth_openid_connect/pull/43)
- Add raw info for id token [#42](https://github.com/m0n9oose/omniauth_openid_connect/pull/42)
- Fixed `id_token` verification when `id_token` is not used [#41](https://github.com/m0n9oose/omniauth_openid_connect/pull/41)
- Cast `response_type` to string when checking if it is set in params [#36](https://github.com/m0n9oose/omniauth_openid_connect/pull/36)
- Support both symbol and string version of `response_type` option [#35](https://github.com/m0n9oose/omniauth_openid_connect/pull/35)
- Fix gemspec homepage [#33](https://github.com/m0n9oose/omniauth_openid_connect/pull/33)
- Add support for `response_type` `id_token` [#32](https://github.com/m0n9oose/omniauth_openid_connect/pull/32)

# v0.3.2 (03.08.2019)

- Use response_mode in `authorize_uri` if the option is defined [#30](https://github.com/m0n9oose/omniauth_openid_connect/pull/30)
- Move verification of `id_token` to before accessing tokens [#28](https://github.com/m0n9oose/omniauth_openid_connect/pull/28)
- Update omniauth dependency [#26](https://github.com/m0n9oose/omniauth_openid_connect/pull/26)

# v0.3.1 (08.06.2019)

- Set default OmniAuth name to openid_connect [#23](https://github.com/m0n9oose/omniauth_openid_connect/pull/23)

# v0.3.0 (27.04.2019)

- RP-Initiated Logout phase [#5](https://github.com/m0n9oose/omniauth_openid_connect/pull/5)
- Allows `ui_locales`, `claims_locales` and `login_hint` as request params [#6](https://github.com/m0n9oose/omniauth_openid_connect/pull/6)
- Make uid label configurable [#11](https://github.com/m0n9oose/omniauth_openid_connect/pull/11)
- Allow rails applications to handle state mismatch [#14](https://github.com/m0n9oose/omniauth_openid_connect/pull/14)
- Handle errors when fetching access_token at callback_phase [#17](https://github.com/m0n9oose/omniauth_openid_connect/pull/17)
- Allow state method to receive env [#19](https://github.com/m0n9oose/omniauth_openid_connect/pull/19)

# v0.2.4 (06.01.2019)

- Prompt and login hint [#4](https://github.com/m0n9oose/omniauth_openid_connect/pull/4)
- Bump openid_connect dependency [#9](https://github.com/m0n9oose/omniauth_openid_connect/pull/9)


# UNRELEASED

CORE-7692: Update openid_connect version for Rails 5+ compatibility

# 0.2.2 (505/26/2015)

- Remove version constraint on openid_connect
- Initial Fork
