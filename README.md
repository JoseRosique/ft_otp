<a href="https://github.com/JaeSeoKim/badge42"><img src="https://badge42.vercel.app/api/v2/cl4qxms4g001609l49j835g66/project/3071725" alt="joslopez's 42 ft_otp Score" /></a>
<h2>Mandatory Part</h2> <p>In the language of your choice, you must implement a program that allows you to register an initial password, and is capable of generating a new password each time it is requested. You can use any library that facilitates the implementation of the algorithm, as long as they do not do the dirty work, that is, it is strictly forbidden to use any TOTP library. Of course, you can and should make use of some library or function that allows you to access [system time].</p> <p>An example of the use of the program would be:</p> <ul> <li>The program should be called ft_otp</li> <li>With the -g option, the program will receive as an argument a [hexadecimal key] of at least 64 characters. The program will safely store this key in a file called ft_otp.key, which will be encrypted.</li> <li>With the -k option, the program will generate a new [temporary password] and print it to standard output.</li> </ul> <code>$ echo -n "NEVER GONNA GIVE YOU UP" > key.txt</code><br> <code>$ ./ft_otp -g key.txt</code><br> <code>./ft_otp: error: key must be 64 hexadecimal characters.</code><br> <code>$ xxd -p key.txt > key.hex</code><br> <code>$ cat key.hex | wc -c</code><br> <code>64</code><br> <code>$ ./ft_otp -g key.hex</code><br> <code>Key was successfully saved in ft_otp.key.</code><br> <code>$ ./ft_otp -k ft_otp.key</code><br> <code>836492</code><br> <code>$ sleep 60</code><br> <code>$ ./ft_otp -k ft_otp.key</code><br> <code>123518</code><br> <p>You can check if your program is working properly by comparing generated passwords with Oathtool or any tool of your choice.</p>  <h2>Bonus Part</h2> <p>The evaluation of the bonuses will be done IF AND ONLY IF the mandatory part is PERFECT. Otherwise, the bonuses will be totally IGNORED.</p> <p>You can enhance your project with the following features:</p> <ul> <li>Allow to choose the [encryption password] of the [master key] ft_otp.key and request it every time a new password is generated.</li> <li>Develop a client that generates the [master password] and validates the results with a graphical interface.</li> <li>Any other features you think are genuinely useful. Your peers will judge if they are so.</li> </ul>
