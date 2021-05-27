---
title: تكامل الملاحظات
description: يوضح هذا الموضوع تكامل بيانات الملاحظات في الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ed068f4264269334babec9acd59d9d58551333b4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018376"
---
# <a name="note-integration"></a><span data-ttu-id="3f9d1-103">تكامل الملاحظات</span><span class="sxs-lookup"><span data-stu-id="3f9d1-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3f9d1-104">أثناء عمليات الأعمال، عادة ما يجمع مستخدمو Microsoft Dynamics 365 معلومات حول عملائهم.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="3f9d1-105">يتم تسجيل هذه المعلومات كأنشطة وملاحظات.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="3f9d1-106">يوضح هذا الموضوع تكامل بيانات الملاحظات في الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="3f9d1-107">يمكن تصنيف معلومات العميل بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="3f9d1-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="3f9d1-108">**المعلومات القابلة للتنفيذ التي يتعامل معها مستخدم Dynamics 365 بالنيابة عن عميل** – على سبيل المثال، Contoso (مستخدم Dynamics 365) يقوم بإجراء عرض لعبة.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="3f9d1-109">يرغب أحد عملاء Contoso (عميل) في حضور عرض اللعبة.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="3f9d1-110">يطلب العميل من أحد موظفي Contoso حجز فتحة في عرض ألعاب له.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="3f9d1-111">يحدث الحجز في تقويم حضور الحدث الخاص بـ Contoso.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="3f9d1-112">**معلومات قابل للتنفيذ لمستخدم Dynamics 365** -على سبيل المثال، أدخل العميل الذي يشتري وحدة Surface إرشادات خاصة تشير إلى أنه يجب تغليف الجهاز كهدية قبل التسليم.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="3f9d1-113">وهذه الإرشادات عبارة عن معلومات قابلة للتنفيذ يجب أن تتم معالجتها بواسطة موظف Contoso المسؤول عن التعبئة.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="3f9d1-114">**معلومات غير قابلة للتنفيذ** – على سبيل المثال، يقوم عميل بزيارة متجر Contoso وفي أثناء المحادثة مع موظف المتجر، أعرب عن اهتمامه بألعاب *Halo* وإكسسوارات الألعاب.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="3f9d1-115">ويقوم موظف المتجر بإنشاء ملاحظة بهذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="3f9d1-116">بعد ذلك يستخدم محرك توصيات المنتجات هذه الملاحظة لإنشاء توصيات للعميل.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="3f9d1-117">بشكل عام، يتم التقاط المعلومات القابلة للتنفيذ كـ *أنشطة* في تطبيقات Finance and Operations وتطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="3f9d1-118">يتم التقاط المعلومات غير القابلة للتنفيذ كـ *ملاحظات* في تطبيقات Finance and Operations و *تعليقات توضيحية* في تطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="3f9d1-119">على الرغم من أن الملاحظات تتكون مخصصة للمعلومات غير القابلة للتنفيذ، إلا أن التطبيقات لن تمنعك من استخدامها لتخزين ومعالجة المعلومات القابلة للتنفيذ إذا كنت ترغب في استخدامها بهذه الطريقة.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="3f9d1-120">تقوم Microsoft حاليًا بإطلاق وظيفة لتكامل الملاحظات.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="3f9d1-121">(سيتم إصدار وظيفة تكامل النشاط لاحقا.) يتوفر تكامل الإشعارات للعملاء والموردين وأوامر المبيعات وأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="3f9d1-122">إنشاء ملاحظة في تطبيق Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="3f9d1-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="3f9d1-123">لإنشاء ملاحظة في تطبيق Customer Engagement ثم مزامنتها إلى أحد تطبيقات Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="3f9d1-124">في تطبيق Customer Engagement، افتح سجل الحساب لأحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="3f9d1-125">في جزء **المخطط الزمني**، حدد علامة الجمع (**+**) ، ثم حدد **ملاحظة** لإنشاء ملاحظة.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![إنشاء ملاحظة في تطبيق Customer Engagement](media/notes-ce-1.png)

3. <span data-ttu-id="3f9d1-127">أدخل عنوانًا ووصفًا، ثم حدد **إضافة ملاحظة**.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-127">Enter a title and description, and then select **Add note**.</span></span>

    ![إدخال عنوان ووصف](media/notes-ce-2.png)

    <span data-ttu-id="3f9d1-129">تتم إضافة الملاحظة الجديدة إلى المخطط الزمني للعميل.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-129">The new note is added to the customer timeline.</span></span>

    ![ملاحظه جديدة في المخطط الزمني للعميل](media/notes-ce-3.png)

4. <span data-ttu-id="3f9d1-131">قم بتسجيل الدخول إلى تطبيقات Finance and Operations، وافتح سجل العميل نفسه.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="3f9d1-132">لاحظ أن **زر المرفقات** (رمز المشبك) الموجود في الركن الأيمن العلوي يشير إلى أن السجل يحتوي على مرفق.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![إخطار حول مرفق](media/notes-ce-4.png)

5. <span data-ttu-id="3f9d1-134">حدد زر **المرفقات** لفتح صفحة **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="3f9d1-135">يجب عليك العثور على الملاحظة التي قمت بإنشاءها في تطبيق Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-135">You should find the note that you created in the customer engagement app.</span></span>

    ![ملاحظة من تطبيق Customer Engagement](media/notes-ce-5.png)

<span data-ttu-id="3f9d1-137">تتم مزامنة أية تحديثات تمت على الملاحظات ذهابًا وإيابًا بين تطبيق Finance and Operations وتطبيق Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="3f9d1-138">إنشاء ملاحظة في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3f9d1-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="3f9d1-139">يمكنك أيضًا إنشاء ملاحظة في تطبيق Finance and Operations، وسوف تتم مزامنتها إلى أحد تطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="3f9d1-140">لإنشاء ملاحظة في تطبيق Finance and Operations ثم مزامنتها إلى أحد تطبيقات Customer Engagement، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="3f9d1-141">في تطبيق Finance and Operations، من صفحة **المرفقات**، حدد **جديد** \> **ملاحظة**.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![إنشاء ملاحظة في تطبيق Finance and Operations](media/notes-fo-1.png)

2. <span data-ttu-id="3f9d1-143">قم بإدخال عنوان ومجموعة مختصرة من التعليمات، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![إدخال عنوان وتعليمات](media/notes-fo-2.png)

3. <span data-ttu-id="3f9d1-145">في تطبيق Customer Engagement، قم بتحديث السجل.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="3f9d1-146">يجب العثور على الملاحظة الجديدة في المخطط الزمني.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-146">You should find the new note on the timeline.</span></span>

    ![ملاحظة جديدة في المخطط الزمني في تطبيق Customer Engagement](media/notes-fo-3.png)

<span data-ttu-id="3f9d1-148">يمكنك تصنيف ملاحظة على أنها داخلية أو خارجية.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="3f9d1-149">في تطبيق Finance and Operations، في صفحة **المرفقات**، افتح الملاحظة، ثم في حقل **القيد**، حدد **داخلي** أو **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![حقل القيد](media/notes-fo-4.png)

<span data-ttu-id="3f9d1-151">يُمكنك أيضًا إنشاء عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-151">You can also create a URL.</span></span>

1. <span data-ttu-id="3f9d1-152">في تطبيق Finance and Operations، من صفحة **المرفقات**، حدد **جديد** \> **URL**.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="3f9d1-153">أدخل عنوانًا وURL.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="3f9d1-154">في حقل **القيد**، حدد **داخلي** أو **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![إنشاء URL في تطبيق Finance and Operations](media/notes-fo-5.png)

4. <span data-ttu-id="3f9d1-156">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-156">Select **Save**.</span></span>

    <span data-ttu-id="3f9d1-157">نظرا لأن تطبيقات Customer Engagement لا تحتوي على نوع URL، يتم دمج عنوان URL مع الكتابة المزدوجة كملاحظة.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![ظهور URL كملاحظة في تطبيق Customer Engagement](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="3f9d1-159">لا يتم دعم مرفقات الملف.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="3f9d1-160">القوالب</span><span class="sxs-lookup"><span data-stu-id="3f9d1-160">Templates</span></span>

<span data-ttu-id="3f9d1-161">يشتمل تكامل الملاحظات على مجموعة من مخططات الجداول تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="3f9d1-162">تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3f9d1-162">Finance and Operations app</span></span> | <span data-ttu-id="3f9d1-163">تطبيق Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="3f9d1-163">Customer engagement app</span></span> | <span data-ttu-id="3f9d1-164">الوصف</span><span class="sxs-lookup"><span data-stu-id="3f9d1-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="3f9d1-165">مرفقات العملاء</span><span class="sxs-lookup"><span data-stu-id="3f9d1-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="3f9d1-166">تعليقات توضيحية</span><span class="sxs-lookup"><span data-stu-id="3f9d1-166">Annotations</span></span> | <span data-ttu-id="3f9d1-167">الأعمال التي تستخدم النصوص العادية وعناوين URL لالتقاط المعلومات الخاصة بالعميل (لكل من المؤسسات والأشخاص).</span><span class="sxs-lookup"><span data-stu-id="3f9d1-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="3f9d1-168">مرفقات مستندات المورّد</span><span class="sxs-lookup"><span data-stu-id="3f9d1-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="3f9d1-169">تعليقات توضيحية</span><span class="sxs-lookup"><span data-stu-id="3f9d1-169">Annotations</span></span> | <span data-ttu-id="3f9d1-170">الأعمال التي تستخدم النصوص العادية وعناوين URL لالتقاط المعلومات الخاصة بالمورد (لكل من المؤسسات والأشخاص).</span><span class="sxs-lookup"><span data-stu-id="3f9d1-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="3f9d1-171">مرفقات مستند رأس أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="3f9d1-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="3f9d1-172">تعليقات توضيحية</span><span class="sxs-lookup"><span data-stu-id="3f9d1-172">Annotations</span></span> | <span data-ttu-id="3f9d1-173">الأعمال التي تستخدم النصوص العادية وعناوين URL للتقاط معلومات خاصة بأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="3f9d1-174">مرفقات مستند رأس أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="3f9d1-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="3f9d1-175">تعليقات توضيحية</span><span class="sxs-lookup"><span data-stu-id="3f9d1-175">Annotations</span></span> | <span data-ttu-id="3f9d1-176">الأعمال التي تستخدم النصوص العادية وعناوين URL للتقاط معلومات خاصة بأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3f9d1-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="3f9d1-177">لمزيد من المعلومات، راجع [مرجع تعيين الكتابة المزدوجة](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3f9d1-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
