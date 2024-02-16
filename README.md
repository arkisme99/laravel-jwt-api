## Instalasi Laravel API With JWT

<ul>
    <li>composer install</li>
    <li>copy .env.example to .env</li>
    <li>setup database</li>
    <li>execute: php artisan migrate</li>
    <li>execute: php key generate</li>
    <li>execute: php artisan jwt:secret</li>
</ul>

## Testing On Postman

<h5>REGISTER USER</h5>
<table>
    <tr>
        <th>URL (POST)</th>
        <th>/api/register</th>
    </tr>
    <tr>
        <td colspan="2">Body (URLEncoded form data)</td>
    </tr>
    <tr>
        <td>name</td>
        <td>required</td>
    </tr>
    <tr>
        <td>email</td>
        <td>required|unique</td>
    </tr>
    <tr>
        <td>password</td>
        <td>required|min:8|confirm</td>
    </tr>
    <tr>
        <td>password_confirmation</td>
        <td>required</td>
    </tr>
</table>

<h5>LOGIN USER</h5>
<table>
    <tr>
        <th>URL (POST)</th>
        <th>/api/login</th>
    </tr>
    <tr>
        <td colspan="2">Body (URLEncoded form data)</td>
    </tr>
    <tr>
        <td>email</td>
        <td>required|unique</td>
    </tr>
    <tr>
        <td>password</td>
        <td>required</td>
    </tr>
</table>

<h5>GET USER LOGIN</h5>
<table>
    <tr>
        <th>URL (GET)</th>
        <th>/api/user</th>
    </tr>
    <tr>
        <td colspan="2">Header</td>
    </tr>
    <tr>
        <td>Accept</td>
        <td>application/json</td>
    </tr>
    <tr>
        <td>Content-Type</td>
        <td>application/json</td>
    </tr>
    <tr>
        <td>Authorization</td>
        <td>Bearer <i>token</i></td>
    </tr>
</table>

<h5>LOGOUT USER</h5>
<table>
    <tr>
        <th>URL (POST)</th>
        <th>/api/logout</th>
    </tr>
    <tr>
        <td colspan="2">Header</td>
    </tr>
    <tr>
        <td>Accept</td>
        <td>application/json</td>
    </tr>
    <tr>
        <td>Content-Type</td>
        <td>application/json</td>
    </tr>
    <tr>
        <td>Authorization</td>
        <td>Bearer <i>token</i></td>
    </tr>
</table>