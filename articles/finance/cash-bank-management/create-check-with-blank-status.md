---
title: إنشاء شيكات بالحالة فارغ
description: يوضح هذا الموضوع كيفية إنشاء شيكات فارغة لحساب بنكي في صفحة الشيكات.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: af79dd4831f2e7fc71c296922d73a9e42f7955b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175815"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="83856-103">إنشاء شيكات بالحالة فارغ</span><span class="sxs-lookup"><span data-stu-id="83856-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="83856-104">يوضح هذا الموضوع كيفية إنشاء شيكات فارغة.</span><span class="sxs-lookup"><span data-stu-id="83856-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="83856-105">على سبيل المثال، قد تقوم بإنشاء شيك فارغ لتسجيل شيك تالف ولا يمكن استخدامه للدفع.</span><span class="sxs-lookup"><span data-stu-id="83856-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="83856-106">في صفحة **الشيكات**، تقوم بمهام صيانة الشيكات.</span><span class="sxs-lookup"><span data-stu-id="83856-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="83856-107">على سبيل المثال، يمكنك إنشاء أرقام شيكات جديدة وحذف الشيكات.</span><span class="sxs-lookup"><span data-stu-id="83856-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="83856-108">يمكنك أيضا إنشاء شيكات بالحالة **فارغ**.</span><span class="sxs-lookup"><span data-stu-id="83856-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="83856-109">بعد إنشاء الشيكات الفارغة، لا يمكن حذفها أو إعادة استخدامها في النظام.</span><span class="sxs-lookup"><span data-stu-id="83856-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="83856-110">لا تتوفر هذه الميزة إلا في صفحة **الشيكات** إذا قمت بتشغيل ميزة **"إنشاء شيكات بالحالة فارغ** في صفحة **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="83856-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="83856-111">في حالة عدم تشغيل الميزة، لا يمكن إنشاء الشيكات بالحالة **فارغ** إلا من خلال مربع حوار **‏‫الدفع بشيك** أثناء عملية تكوين الدفع في الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="83856-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="83856-112">لفتح صفحة **الشيكات**، انتقل إلى **إدارة النقد والبنوك \> حسابات بنكية \> حسابات بنكية**، ثم في جزء الإجراءات ضمن علامة تبويب **إدارة المدفوعات**، في مجموعة **المعلومات المرتبطة**، حدد **شيكات**.</span><span class="sxs-lookup"><span data-stu-id="83856-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="83856-113">أو انتقل بدلاً من ذلك إلى **إدارة النقد والبنوك \> استعلامات وتقارير \> شيكات**.</span><span class="sxs-lookup"><span data-stu-id="83856-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="83856-114">ولإنشاء الشيكات بالحالة **فارغ** حدد **إنشاء شيكات فارغة** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="83856-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="83856-115">بينما يقوم النظام بإنشاء شيكات فارغة، يتم إلغاء تنشيط الحساب البنكي المقترن مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="83856-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="83856-116">يقلل هذا السلوك المخاطرة الناجمة عن تلك المدفوعات في نفس الوقت الذي يتم فيه إنشاء شيكات فارغه.</span><span class="sxs-lookup"><span data-stu-id="83856-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="83856-117">عند إتمام المعالجة، تتم إعادة تنشيط الحساب البنكي المقترن.</span><span class="sxs-lookup"><span data-stu-id="83856-117">When the processing is completed, the associated bank account is reactivated.</span></span>
