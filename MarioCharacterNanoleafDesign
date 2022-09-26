import nanoleafapi as nl
import time

ips = ["192.168.1.14", "192.168.1.13", "192.168.1.12", "192.168.1.10", "192.168.1.11", "192.168.1.9", "192.168.1.4", "192.168.1.5", "192.168.1.3", "192.168.1.2"]

auths = ['4xjvV9IJAQDq83SFaROVVzvble3vHwV8', 'LlBI3Odz7EOHR3v5TPwh4fDbGrFuKSq7', 'WKiepsgP7vhnfI4zGBmxVH26Rq6KNFgg', '28vOnfDhQZXeShXjGKWocxHZJUe9NCwn', 'vioLVKiV1IgfsAA94JFFBTFy0vEUG48K', 'UY3DEDumg19xCnwrNV4Btm2FPF0CAhdO', '0AJgQMml89aa12iAYpAqEoWKrKW18JZa', '5EpekYkcVupgIjXM37bRsNG0pE38NfGC', 'cSTCTsuAgBRC7i8F3ug1cc1Z1smDyPQH', 'kAbYywuZWBWsMrFsOluxbnqAXEQqyMKr']

controllers = [0] * len(ips)

# A simple for loop initializes all of the Nanoleaf objects into a list of 10
for i in range(len(ips)):
    controllers[i] = nl.Nanoleaf(ips[i], auths[i])

for controller in controllers:
    controller.set_brightness(100)
digital_twin = [0] * len(controllers)

for i, controller in enumerate(controllers):
    digital_twin[i] = nl.digital_twin.NanoleafDigitalTwin(controller)

# The following lists (and lists of lists) are the panel id's for the nanoleaf panels. This allows the values to be easily accessed.
# These value were found in an external script.

controller0 = [[102, 101, 100, 99, 98, 97, 96, 95, 94, 93, 92, 91, 90],

[74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 87, 88, 89]]

controller1 = [69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 9, 10, 11, 16]

controller2 = [44, 45, 46, 15, 19, 18, 17, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58]

controller3 = [38, 37, 36, 88, 89, 90, 91, 17, 13, 12, 11, 10, 92, 93, 94, 18, 95, 96, 41, 45, 97]

controller4 = [56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78]

controller5 = [69, 71, 78, 70, 64, 68, 85, 59, 79, 73, 80, 61, 33, 72, 67, 63, 62, 17, 65, 66, 75, 77, 31]

controller6 = [70, 52, 53, 54, 55, 56, 57, 58, 59, 17, 18, 60, 61, 62, 63, 64, 65, 66, 67, 68, 71]

controller7 = [75, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 76, 78, 79]

controller8 = [69, 59, 60, 131, 38, 37, 61, 62, 63, 65, 66, 67, 22, 21, 20, 19, 68]

controller9 = [[39, 98, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 100],
[75, 55, 97, 96, 95, 94, 93, 92, 91, 90, 89, 10, 88]]

'''setting colors in RGB'''
#common colours
black = (0, 0, 0)
background_green = (0, 204, 0)
background_brown = (153, 76, 0)
background_white = (255, 255, 255)

#mario colours
mario_red = (255, 0, 0)
mario_brown = (102, 51, 0)
mario_blue = (0, 0, 255)
mario_skin = (255, 178, 102)

#luigi colours
luigi_green = (0, 204, 0)
luigi_brown = (102, 51, 0)
luigi_blue = (0, 0, 255)
luigi_skin = (255, 178, 102)

#flower colours
plant_red = (255, 0, 0)
star_yellow = (255, 205, 60) 
tube_green = (44, 176, 26)

#peach colours
peach_crown = (153, 153, 0)
peach_yellow = (255, 255, 0)
peach_pink = (255, 0, 127)
peach_skin = (255, 229, 204)

#toad colours
toad_red = (255, 0, 0)
toad_blue = (51, 51, 255)
toad_brown = (112, 70, 33)
toad_skin = (255, 204, 153)

'''the following line loops the images continually'''
i = True 
while i == True:

    [controller.set_effect('') for controller in controllers]       #sets effect

    '''mario'''
    [x.set_all_colors((0, 255, 255)) for x in digital_twin]          #sets background colour

    [digital_twin[0].set_color(x, mario_red) for x in controller0[1][4:13]]

    [digital_twin[1].set_color(x, mario_brown) for x in controller1[4:8]]
    [digital_twin[1].set_color(x, mario_skin) for x in controller1[8:10]]
    [digital_twin[1].set_color(x, black) for x in controller1[10:11]]
    [digital_twin[1].set_color(x, mario_skin) for x in controller1[11:13]]

    [digital_twin[2].set_color(x, mario_brown) for x in controller2[5:7]]
    [digital_twin[2].set_color(x, mario_skin) for x in controller2[7:14]]
    [digital_twin[2].set_color(x, mario_brown) for x in controller2[12:14]]
    [digital_twin[2].set_color(x, background_white) for x in controller2[16:]]

    [digital_twin[3].set_color(x, background_white) for x in controller3[2:5]]
    [digital_twin[3].set_color(x, mario_skin) for x in controller3[7:14]]

    [digital_twin[4].set_color(x, mario_red) for x in controller4[8:15:3]]
    [digital_twin[4].set_color(x, mario_blue) for x in controller4[9:11]]
    [digital_twin[4].set_color(x, mario_blue) for x in controller4[12:14]]
    [digital_twin[4].set_color(x, background_white) for x in controller4[16:19]]

    [digital_twin[5].set_color(x, mario_red) for x in controller5[7:9]]
    [digital_twin[5].set_color(x, mario_red) for x in controller5[14:16]]
    [digital_twin[5].set_color(x, mario_blue) for x in controller5[9:14]]

    [digital_twin[6].set_color(x, mario_skin) for x in controller6[5:7]]
    [digital_twin[6].set_color(x, mario_skin) for x in controller6[14:16]]
    [digital_twin[6].set_color(x, mario_blue) for x in controller6[7:14]]

    [digital_twin[7].set_color(x, mario_blue) for x in controller7[5:9]]
    [digital_twin[7].set_color(x, mario_blue) for x in controller7[10:14]]

    [digital_twin[8].set_color(x, mario_brown) for x in controller8[3:7]]
    [digital_twin[8].set_color(x, mario_brown) for x in controller8[10:14]]

    [digital_twin[9].set_color(x, background_green) for x in controller9[0][0:]]
    [digital_twin[9].set_color(x, background_brown) for x in controller9[1][0:]]

    [x.sync() for x in digital_twin]            #syncs code above with the panel
    [x.sync() for x in digital_twin]            #syncs code above with the panel again in case of error

    time.sleep(6)               #sets a timer of six seconds between images
    [controller.set_effect(' ') for controller in controllers]              #sets an effect of falling between images

    '''peach'''

    [x.set_all_colors((0, 255, 255)) for x in digital_twin]
 
    [digital_twin[0].set_color(x, peach_crown) for x in controller0[0][4:9:2]] #crown
    [digital_twin[0].set_color(x, peach_yellow) for x in controller0[1][4:11]] #hair

    [digital_twin[1].set_color(x, peach_yellow) for x in controller1[4:6]] #hair
    [digital_twin[1].set_color(x, peach_skin) for x in controller1[6:10]]
    [digital_twin[1].set_color(x, black) for x in controller1[10:11]]
    [digital_twin[1].set_color(x, peach_skin) for x in controller1[11:13]]

    [digital_twin[2].set_color(x, peach_yellow) for x in controller2[4:6]]
    [digital_twin[2].set_color(x, peach_skin) for x in controller2[6:14]]
    [digital_twin[2].set_color(x, background_white) for x in controller2[16:19]] #cloud 

    [digital_twin[3].set_color(x, peach_yellow) for x in controller3[4:7]]
    [digital_twin[3].set_color(x, peach_skin) for x in controller3[7:14]]
    [digital_twin[3].set_color(x, background_white) for x in controller3[2:4]] #cloud 

    [digital_twin[4].set_color(x, peach_yellow) for x in controller4[5:8]]
    [digital_twin[4].set_color(x, peach_pink) for x in controller4[8:10]]
    [digital_twin[4].set_color(x, peach_skin) for x in controller4[10:13]]
    [digital_twin[4].set_color(x, peach_pink) for x in controller4[13:15]]
    [digital_twin[4].set_color(x, background_white) for x in controller4[16:19]] #cloud 

    [digital_twin[5].set_color(x, peach_pink) for x in controller5[7:16]]

    [digital_twin[6].set_color(x, peach_skin) for x in controller6[5:7]]
    [digital_twin[6].set_color(x, peach_pink) for x in controller6[7:14]]
    [digital_twin[6].set_color(x, peach_skin) for x in controller6[14:16]]

    [digital_twin[7].set_color(x, peach_pink) for x in controller7[5:14]]

    [digital_twin[8].set_color(x, peach_pink) for x in controller8[3:14]]

    [digital_twin[9].set_color(x, background_green) for x in controller9[0][0:15]] #grass
    [digital_twin[9].set_color(x, background_brown) for x in controller9[1][0:13]] #dirt

    [x.sync() for x in digital_twin]            #syncs code above with the panel
    [x.sync() for x in digital_twin]            #syncs code above with the panel again in case of error

    time.sleep(6)               #sets a timer of six seconds between images
    [controller.set_effect(' ') for controller in controllers]              #sets an effect of falling between images

    '''luigi'''

    [x.set_all_colors((0, 255, 255)) for x in digital_twin]          #sets background colour

    [digital_twin[0].set_color(x, luigi_green) for x in controller0[1][4:13]]

    [digital_twin[1].set_color(x, luigi_brown) for x in controller1[4:8]]
    [digital_twin[1].set_color(x, luigi_skin) for x in controller1[8:10]]
    [digital_twin[1].set_color(x, black) for x in controller1[10:11]]
    [digital_twin[1].set_color(x, luigi_skin) for x in controller1[11:13]]

    [digital_twin[2].set_color(x, luigi_brown) for x in controller2[5:7]]
    [digital_twin[2].set_color(x, luigi_skin) for x in controller2[7:14]]
    [digital_twin[2].set_color(x, black) for x in controller2[12:14]]
    [digital_twin[2].set_color(x, background_white) for x in controller2[16:]]

    [digital_twin[3].set_color(x, background_white) for x in controller3[2:5]]
    [digital_twin[3].set_color(x, luigi_skin) for x in controller3[7:14]]

    [digital_twin[4].set_color(x, luigi_green) for x in controller4[8:15:3]]
    [digital_twin[4].set_color(x, luigi_blue) for x in controller4[9:11]]
    [digital_twin[4].set_color(x, luigi_blue) for x in controller4[12:14]]
    [digital_twin[4].set_color(x, background_white) for x in controller4[16:19]]

    [digital_twin[5].set_color(x, luigi_green) for x in controller5[7:9]]
    [digital_twin[5].set_color(x, luigi_green) for x in controller5[14:16]]
    [digital_twin[5].set_color(x, luigi_blue) for x in controller5[9:14]]

    [digital_twin[6].set_color(x, background_white) for x in controller6[5:7]]
    [digital_twin[6].set_color(x, background_white) for x in controller6[14:16]]
    [digital_twin[6].set_color(x, luigi_blue) for x in controller6[7:14]]

    [digital_twin[7].set_color(x, luigi_blue) for x in controller7[5:9]]
    [digital_twin[7].set_color(x, luigi_blue) for x in controller7[10:14]]

    [digital_twin[8].set_color(x, luigi_brown) for x in controller8[3:7]]
    [digital_twin[8].set_color(x, luigi_brown) for x in controller8[10:14]]

    [digital_twin[9].set_color(x, background_green) for x in controller9[0][0:]]
    [digital_twin[9].set_color(x, background_brown) for x in controller9[1][0:]]

    # This final line syncs the digital twin with the actual controllers, applying everything set up before.

    [x.sync() for x in digital_twin]            #syncs code above with the panel
    [x.sync() for x in digital_twin]            #syncs code above with the panel again in case of error

    time.sleep(6)               #sets a timer of six seconds between images
    [controller.set_effect(' ') for controller in controllers]              #sets an effect of falling between images

    '''toad'''

    [x.set_all_colors((0, 255, 255)) for x in digital_twin]          #sets background colour

    [digital_twin[0].set_color(x, toad_red) for x in controller0[0][2:4]]
    [digital_twin[0].set_color(x, toad_red) for x in controller0[0][8:11]]
    [digital_twin[0].set_color(x, background_white) for x in controller0[0][4:8]]
    [digital_twin[0].set_color(x, toad_red) for x in controller0[1][9:12]]
    [digital_twin[0].set_color(x, background_white) for x in controller0[1][2:9]]
    [digital_twin[0].set_color(x, background_white) for x in controller0[1][12:13]]

    [digital_twin[1].set_color(x, background_white) for x in controller1[3:6]]
    [digital_twin[1].set_color(x, background_white) for x in controller1[9:14]]
    [digital_twin[1].set_color(x, toad_red) for x in controller1[6:9]]

    [digital_twin[2].set_color(x, background_white) for x in controller2[5:7]]
    [digital_twin[2].set_color(x, background_white) for x in controller2[10:14]]
    [digital_twin[2].set_color(x, background_white) for x in controller2[16:]]
    [digital_twin[2].set_color(x, toad_red) for x in controller2[7:10]]

    [digital_twin[3].set_color(x, background_white) for x in controller3[2:5]]
    [digital_twin[3].set_color(x, toad_skin) for x in controller3[9:12]]
    [digital_twin[3].set_color(x, black) for x in controller3[8:13:4]]

    [digital_twin[4].set_color(x, toad_skin) for x in controller4[9:14]]
    [digital_twin[4].set_color(x, background_white) for x in controller4[16:19]]

    [digital_twin[5].set_color(x, toad_skin) for x in controller5[7:9]]
    [digital_twin[5].set_color(x, toad_skin) for x in controller5[11:12]]
    [digital_twin[5].set_color(x, toad_skin) for x in controller5[14:16]]
    [digital_twin[5].set_color(x, toad_blue) for x in controller5[9:11]]
    [digital_twin[5].set_color(x, toad_blue) for x in controller5[12:14]]

    [digital_twin[6].set_color(x, toad_skin) for x in controller6[5:7]]
    [digital_twin[6].set_color(x, toad_skin) for x in controller6[10:11]]
    [digital_twin[6].set_color(x, toad_skin) for x in controller6[14:16]]
    [digital_twin[6].set_color(x, toad_blue) for x in controller6[8:10]]
    [digital_twin[6].set_color(x, toad_blue) for x in controller6[11:13]]

    [digital_twin[7].set_color(x, background_white) for x in controller7[7:12]]

    [digital_twin[8].set_color(x, toad_brown) for x in controller8[5:12:6]]
    [digital_twin[8].set_color(x, background_white) for x in controller8[6:11]]

    [digital_twin[9].set_color(x, background_green) for x in controller9[0][0:]]
    [digital_twin[9].set_color(x, background_brown) for x in controller9[1][0:]]

    [x.sync() for x in digital_twin]            #syncs code above with the panel
    [x.sync() for x in digital_twin]            #syncs code above with the panel again in case of error

    time.sleep(6)               #sets a timer of six seconds between images
    [controller.set_effect(' ') for controller in controllers]              #sets an effect of falling between images

    '''flower'''
    
    [x.set_all_colors((0, 255, 255)) for x in digital_twin]          #sets background colour

    [digital_twin[0].set_color(x, background_white) for x in controller0[1][2:5]]
    [digital_twin[0].set_color(x, background_white) for x in controller0[1][10:13]]

    [digital_twin[1].set_color(x, plant_red) for x in controller1[6:11:4]]

    [digital_twin[2].set_color(x, star_yellow) for x in controller2[2:3]]
    [digital_twin[2].set_color(x, star_yellow) for x in controller2[16:17]]
    [digital_twin[2].set_color(x, plant_red) for x in controller2[6:13:2]]
    [digital_twin[2].set_color(x, background_white) for x in controller2[7:8]]
    [digital_twin[2].set_color(x, background_white) for x in controller2[11:12]]

    [digital_twin[3].set_color(x, star_yellow) for x in controller3[1:6]]
    [digital_twin[3].set_color(x, star_yellow) for x in controller3[15:20]]
    [digital_twin[3].set_color(x, plant_red) for x in controller3[7:8]]
    [digital_twin[3].set_color(x, plant_red) for x in controller3[13:14]]
    [digital_twin[3].set_color(x, plant_red) for x in controller3[9:12]]
    [digital_twin[3].set_color(x, background_white) for x in controller3[8:13:4]]

    [digital_twin[4].set_color(x, star_yellow) for x in controller4[3:6:2]]
    [digital_twin[4].set_color(x, star_yellow) for x in controller4[17:20:2]]
    [digital_twin[4].set_color(x, plant_red) for x in controller4[9:14]]

    [digital_twin[5].set_color(x, tube_green) for x in controller5[2:7]]
    [digital_twin[5].set_color(x, tube_green) for x in controller5[16:21]]
    [digital_twin[5].set_color(x, background_green) for x in controller5[11:12]]

    [digital_twin[6].set_color(x, tube_green) for x in controller6[2:5]]
    [digital_twin[6].set_color(x, tube_green) for x in controller6[16:19]]
    [digital_twin[6].set_color(x, background_green) for x in controller6[8:13]]

    [digital_twin[7].set_color(x, tube_green) for x in controller7[1:4]]
    [digital_twin[7].set_color(x, tube_green) for x in controller7[15:18]]
    [digital_twin[7].set_color(x, background_green) for x in controller7[9:10]]

    [digital_twin[8].set_color(x, background_green) for x in controller8[8:9]]
    [digital_twin[8].set_color(x, background_brown) for x in controller8[0:8]]
    [digital_twin[8].set_color(x, background_brown) for x in controller8[9:]]

    [digital_twin[9].set_color(x, background_green) for x in controller9[0][4:11]]
    [digital_twin[9].set_color(x, background_brown) for x in controller9[0][0:4]]
    [digital_twin[9].set_color(x, background_brown) for x in controller9[0][11:]]
    [digital_twin[9].set_color(x, background_brown) for x in controller9[1][0:6]]
    [digital_twin[9].set_color(x, background_green) for x in controller9[1][6:7]]
    [digital_twin[9].set_color(x, background_brown) for x in controller9[1][7:]]

    [x.sync() for x in digital_twin]            #syncs code above with the panel
    [x.sync() for x in digital_twin]            #syncs code above with the panel again in case of error

    time.sleep(6)               #sets a timer of six seconds between images
    [controller.set_effect(' ') for controller in controllers]              #sets an effect of falling between images
'''end!'''
