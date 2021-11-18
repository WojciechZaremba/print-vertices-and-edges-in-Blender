obdata = bpy.context.object.data

out = '{'
out += '"vertices":{'
for v in obdata.vertices:
    if v.index < len(obdata.vertices)-1:
        out += ('"{}":[{},{},{}],'.format(v.index, v.co.x, v.co.y, v.co.z))
    else:
        out += ('"{}":[{},{},{}]'.format(v.index, v.co.x, v.co.y, v.co.z))
        
out += '},"edges":{'
for e in obdata.edges:
    if e.index < len(obdata.edges)-1:
        out += ('"{}":[{},{}],'.format(e.index, e.vertices[0], e.vertices[1]))
    else:
        out += ('"{}":[{},{}]'.format(e.index, e.vertices[0], e.vertices[1]))
        out+= '}'
        
out += '}'
print(out,end="")
