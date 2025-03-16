{% if contact.sent %}

<div class="row">
        <div class="col-md-6 col-md-offset-3">
                <p>Your message has been sent and we&#8217;ll get back to you soon.</p>
        </div>
</div>

{% else %}

<div class="row">
        <div class="col-md-3 col-md-offset-3">
        <div class="wetheme-contact-text">        
                <p>Sed vel convallis libero. Phasellus vehicula ut arcu eget elementum. Phasellus eu nisi et leo molestie fermentum quis at tortor. Vivamus sit amet mauris quis ligula hendrerit cursus. Nunc eget aliquam justo. In placerat purus vel maximus vehicula. Donec et consequat quam.</p>

                <p>Etiam fringilla, ipsum vitae ultrices scelerisque, quam dui blandit tellus, vitae malesuada quam nunc eu purus. Curabitur non turpis ultricies, auctor turpis ac, tempor diam. Integer quis arcu enim. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla iaculis dolor at bibendum dapibus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Vivamus sit amet quam id risus tristique fringilla vitae ut ligula. Mauris rutrum maximus nulla ac hendrerit. In hac habitasse platea dictumst.</p>
        </div>
        </div>
        <div class="col-md-3">
                <form method="post" action="/contact">
                        <fieldset>
                                  <div class="col-lg-6">
                                          <ul class="contact-1">
                                            <li class="form-group">
                                              <label for="name">Name</label>
                                              {{ contact | contact_input: 'name' }}
                                            </li>
                                            <li class="form-group">
                                              <label for="email">Email</label>
                                              {{ contact | contact_input: 'email' }}
                                            </li>
                                            <li class="form-group">
                                              <label for="subject">Subject</label>
                                              {{ contact | contact_input: 'subject' }}
                                            </li>
                                            <li class="form-group">
                                              <label for="message">Message</label><br />
                                              <div class="wetheme-contact-textarea">                                              
                                              {{ contact | contact_input: 'message' }}
                                              </div>
                                            </li>
                                            <li class="form-group">
                                              <label for="captcha">Spam check</label>
                                              <p>Please enter the characters from the image.</p>
                                              <div>{{ contact.captcha }}</div>
                                              {{ contact | contact_input: 'captcha' }}
                                            </li>
                                            <li class="form-group">
                                              <button type="submit" class="btn btn-default">Send</button>
                                            </li>
                                    </ul>
                            </div>
                        </fieldset>
                </form>
        </div>
</div>

{% endif %}可以开发功能。
